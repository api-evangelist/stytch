# Stytch GraphQL Schema

## Overview

Stytch is a REST-only authentication and identity platform. No public GraphQL API is offered. This directory contains a **conceptual GraphQL schema** (`stytch-schema.graphql`) derived from Stytch's published REST API surface across three product areas:

- **Consumer Authentication API** — `https://api.stytch.com/v1/`
- **B2B Authentication API** — `https://api.stytch.com/v1/b2b/`
- **Management API** — `https://management.stytch.com/v1/`

Source documentation: <https://stytch.com/docs/api>  
OpenAPI sources: <https://github.com/stytchauth/stytch-openapi>, <https://github.com/stytchauth/stytch-management-openapi>

---

## Schema Source

| Field | Value |
|---|---|
| Schema type | Conceptual (REST-derived) |
| Real GraphQL endpoint | None |
| SDL file | `stytch-schema.graphql` |
| Derived from | Stytch REST OpenAPI specs + public docs |
| Schema date | 2026-06-14 |

---

## Type Inventory

### Consumer API Types

| Type | Description |
|---|---|
| `User` | Core consumer end-user identity record |
| `UserName` | Structured name (first / middle / last) |
| `Email` | Verified email address belonging to a User |
| `PhoneNumber` | Verified phone number belonging to a User |
| `TrustedMetadata` | Operator-controlled JSON metadata on a User |
| `OAuthProviderRecord` | OAuth provider link (Google, Apple, GitHub, etc.) |
| `WebAuthnRegistration` | WebAuthn / Passkey credential registration |
| `TOTPRecord` | TOTP authenticator app registration |
| `CryptoWalletRecord` | Ethereum or Solana wallet linked to a User |
| `BiometricRegistration` | Device-native biometric registration |
| `PasswordRecord` | Bcrypt/argon2 password credential record |
| `Session` | Active consumer session with authentication factors |
| `SessionAttributes` | IP address and user agent recorded at session start |
| `AuthenticationFactor` | A single factor recorded inside a session |
| `MagicLink` | Email magic link send/authenticate result |
| `EmbeddedMagicLink` | Pre-built UI embedded magic link token |
| `OTP` | One-time passcode send result (email, SMS, WhatsApp) |
| `TOTPCreate` | TOTP secret + QR code + recovery codes on creation |
| `OAuthAuthenticate` | OAuth token authenticate result |
| `OAuthProviderValues` | Access/refresh/id tokens from an OAuth provider |
| `Password` | Password credential authenticate/create result |
| `ConnectedApp` | OAuth 2.0 Connected App (Stytch-as-AuthServer) |
| `M2MClient` | Machine-to-machine client credential client |
| `Permission` | A named permission within an RBAC resource |
| `RBACResource` | A resource type that permissions are scoped to |
| `Role` | A role that groups permissions |
| `Policy` | Top-level RBAC policy for a Stytch project |

### B2B API Types

| Type | Description |
|---|---|
| `Organization` | A B2B tenant organization |
| `Member` | A member of a B2B organization |
| `AssignedRole` | A role assigned to a member with its sources |
| `ImplicitRoleAssignment` | Role auto-assigned to members matching an email domain |
| `B2BSession` | Active session for a B2B organization member |
| `SSOConnection` | SSO connection (SAML or OIDC) for an organization |
| `SAMLConnection` | SAML-specific SSO connection configuration |
| `SAMLCertificate` | X.509 signing certificate for a SAML connection |
| `OIDCConnection` | OIDC-specific SSO connection configuration |
| `SCIMConnection` | SCIM directory-sync connection for an organization |
| `SCIMGroupRoleAssignment` | SCIM group mapped to a B2B RBAC role |

### Management API Types

| Type | Description |
|---|---|
| `Project` | A Stytch project (workspace unit) |
| `ProjectEnvironmentConfig` | Live/test environment config per project |
| `Secret` | A Stytch project API secret |

### Enum Types

| Enum | Values |
|---|---|
| `AuthenticationFactorType` | MAGIC_LINK, OTP_EMAIL, OTP_SMS, OTP_WHATSAPP, OAUTH, TOTP, WEBAUTHN, CRYPTO_WALLET, PASSWORD, SSO_SAML, SSO_OIDC, RECOVERY_CODE |
| `OTPChannel` | EMAIL, SMS, WHATSAPP |
| `OAuthProvider` | GOOGLE, APPLE, FACEBOOK, GITHUB, GITLAB, MICROSOFT, SLACK, DISCORD, SALESFORCE, HUBSPOT, LINKEDIN, TWITCH, COINBASE, FIGMA, SNAPCHAT |
| `CryptoWalletType` | ETHEREUM, SOLANA |
| `SessionTokenType` | OPAQUE, JWT |
| `MemberStatus` | ACTIVE, INVITED, PENDING_SELECTION, WITHDRAWN |
| `SSOConnectionType` | SAML, OIDC |
| `SCIMProvisioningStatus` | ACTIVE, NOT_STARTED, STALE |
| `RBACScope` | CONSUMER, B2B |
| `PolicyResourceAccess` | ALLOW, DENY |
| `ProjectEnvironment` | LIVE, TEST |
| `SecretStatus` | ACTIVE, INACTIVE |

---

## Key Design Decisions

**Sessions hold Authentication Factors.** Both `Session` and `B2BSession` embed an `authenticationFactors` list — mirroring how Stytch REST responses return the full factor history, enabling fine-grained MFA policy evaluation in any downstream consumer.

**Consumer vs. B2B split.** `User`/`Session` and `Organization`/`Member`/`B2BSession` are deliberately separate type trees, reflecting Stytch's own product boundary. A `Member` carries an `emailAddress` primary identifier (not a `userId`) consistent with B2B's org-scoped identity model.

**Connected Apps + M2M as first-class types.** Stytch positions its platform as "agent-ready" — Connected Apps (Stytch-as-OAuth-server) and M2M client credentials are modelled as top-level types rather than embedded config, because they are independently managed resources consumed by AI agents and MCP servers.

**SCIM and SSO under Organization.** `SCIMConnection` and `SSOConnection` are typed separately but hang off `Organization`, consistent with Stytch's multi-tenant B2B model where each org manages its own directory-sync and enterprise SSO.

**TrustedMetadata as a wrapper type.** Rather than inlining `JSON` everywhere, operator-controlled metadata is wrapped in `TrustedMetadata` so tooling can distinguish it from `untrustedMetadata` (user-editable) without relying solely on field naming.

---

## References

- REST API reference: <https://stytch.com/docs/api>
- B2B API reference: <https://stytch.com/docs/b2b/api/overview>
- Management API docs: <https://stytch.com/docs/workspace-management-api>
- Consumer OpenAPI: <https://github.com/stytchauth/stytch-openapi>
- Management OpenAPI: <https://github.com/stytchauth/stytch-management-openapi>
- GitHub org: <https://github.com/stytchauth>
