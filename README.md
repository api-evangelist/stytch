# Stytch (stytch)

Stytch is an authentication and identity infrastructure provider. Its Consumer and B2B APIs cover passwordless authentication (Magic Links, OTP, OAuth, WebAuthn / Passkeys, TOTP), enterprise SSO (SAML / OIDC) and SCIM, sessions, M2M client-credentials tokens, and Device Fingerprinting / fraud defense. Connected Apps lets a Stytch-secured product act as an OAuth 2.0 / OIDC Authorization Server for third-party integrations, desktop apps, AI agents, and MCP servers — a posture Stytch describes as "agent-ready". A separate Management API plus a Terraform provider handle workspace configuration as code.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/stytch/refs/heads/main/apis.yml)

## Scope

- **Type:** Contract
- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

Authentication, Identity, Passwordless, Security, B2B, Connected Apps, MCP, AI Agents, Developer Tools

## Timestamps

- **Created:** 2024-11-15
- **Modified:** 2026-05-22

## APIs

### Stytch Consumer Authentication API

Magic Links, SMS / email / WhatsApp OTP, OAuth social login, Passwords, TOTP, WebAuthn / Passkeys, Crypto Wallets, Sessions, Users, M2M, Connected Apps (OAuth provider for AI agents and MCP servers), Fraud / Device Fingerprinting, Impersonation, IDP, and Consumer RBAC. 81 paths.

**Tags:** Authentication, Passwordless, Magic Links, OTP, OAuth, WebAuthn, Passkeys, Consumer, M2M, Connected Apps, Fraud

- [Documentation](https://stytch.com/docs/api)
- [API Reference](https://stytch.com/docs/api/reference/library/overview)
- [OpenAPI](openapi/stytch-consumer-openapi.yml)
- [OpenAPI Source](https://github.com/stytchauth/stytch-openapi)

### Stytch B2B Authentication API

Organizations, Members, SSO (SAML and OIDC), Magic Links, OTP, OAuth, Discovery, Sessions, B2B RBAC, SCIM directory sync, TOTP, Recovery Codes, Passwords, Impersonation, and the B2B IDP surface. 90 paths.

**Tags:** Authentication, B2B, SSO, SAML, OIDC, SCIM, Multi-Tenant, Organizations, RBAC, Connected Apps

- [Documentation](https://stytch.com/docs/b2b)
- [API Reference](https://stytch.com/docs/b2b/api/overview)
- [OpenAPI](openapi/stytch-b2b-openapi.yml)
- [OpenAPI Source](https://github.com/stytchauth/stytch-openapi)

### Stytch Management API

Workspace configuration: projects, environments, secrets, redirect URLs, allowed country codes, RBAC policies, email templates, JWT templates, event log streaming, public tokens, trusted token profiles, and Consumer / B2B SDK configuration. Backs the Terraform provider and language-specific management SDKs. 29 paths.

**Tags:** Management, Configuration, Projects, Secrets, RBAC, SDKConfig

- [Documentation](https://stytch.com/docs/workspace-management-api)
- [OpenAPI](openapi/stytch-management-openapi.yml)
- [OpenAPI Source](https://github.com/stytchauth/stytch-management-openapi)
- [Terraform Provider](https://github.com/stytchauth/terraform-provider-stytch)

---

## Common Properties

- [Website](https://stytch.com)
- [Documentation](https://stytch.com/docs)
- [API Reference](https://stytch.com/docs/api)
- [Sign Up](https://app.stytch.com/register)
- [Portal](https://app.stytch.com)
- [Pricing](https://stytch.com/pricing)
- [Status](https://status.stytch.com)
- [Blog](https://stytch.com/blog)
- [Connected Apps](https://stytch.com/docs/guides/connected-apps/overview)
- [MCP Server Demo](https://github.com/stytchauth/mcp-stytch-consumer-todo-list)
- [is-agent SDK](https://github.com/stytchauth/is-agent)
- [GitHub Organization](https://github.com/stytchauth)
- [Postman Workspace](https://www.postman.com/stytch/stytch-public-workspace/overview)
- [Spectral Rules](rules/stytch-rules.yml)
- [Vocabulary](vocabulary/stytch-vocabulary.yml)
- [Plans & Pricing](plans/stytch-plans-pricing.yml)
- [Rate Limits](rate-limits/stytch-rate-limits.yml)
- [FinOps](finops/stytch-finops.yml)

## Capabilities

| Capability | Description |
|---|---|
| [Passwordless Authentication](capabilities/passwordless-authentication.yaml) | Consumer passwordless auth — Magic Links, OTP, Session Management |
| [B2B Identity Management](capabilities/b2b-identity-management.yaml) | B2B auth — Organizations, Members, SSO, Discovery |
| [B2B SSO & SCIM Provisioning](capabilities/b2b-sso-scim-provisioning.yaml) | Enterprise SSO (SAML/OIDC) + SCIM directory sync |
| [Connected Apps & MCP Authorization](capabilities/connected-apps-mcp-authorization.yaml) | Stand up your product as an OAuth/OIDC Authorization Server for third-party tools, AI agents, and MCP servers |
| [M2M Service Authentication](capabilities/m2m-service-authentication.yaml) | Client-credentials JWT tokens for service-to-service and headless automation |
| [Fraud & Device Intelligence](capabilities/fraud-device-intelligence.yaml) | DFP fingerprint lookup, verdict reasons, adaptive MFA, fraud rules |

## JSON Schemas

- [stytch-user-schema.json](json-schema/stytch-user-schema.json) — Consumer User
- [stytch-organization-schema.json](json-schema/stytch-organization-schema.json) — B2B Organization
- [stytch-member-schema.json](json-schema/stytch-member-schema.json) — B2B Member
- [stytch-connected-app-schema.json](json-schema/stytch-connected-app-schema.json) — Connected App / OAuth client
- [stytch-m2m-client-schema.json](json-schema/stytch-m2m-client-schema.json) — M2M client

## JSON Structures

- [stytch-session-structure.json](json-structure/stytch-session-structure.json) — Session object
- [stytch-connected-app-structure.json](json-structure/stytch-connected-app-structure.json) — Connected App structure

## JSON-LD

- [stytch-context.jsonld](json-ld/stytch-context.jsonld) — Vocabulary mapping (User, Member, Organization, ConnectedApp, MCPServerClient, M2MClient, AIAgent, DeviceFingerprint, FraudVerdict, etc.)

## Examples

- [Send Magic Link](examples/stytch-send-magic-link-example.json)
- [Create B2B Organization](examples/stytch-create-organization-example.json)
- [Consumer Magic Links — Login or Create](examples/stytch-consumer-magic-links-login-or-create-example.json)
- [Consumer OTP — Send SMS](examples/stytch-consumer-otps-sms-send-example.json)
- [Consumer OAuth — Authenticate](examples/stytch-consumer-oauth-authenticate-example.json)
- [Consumer Sessions — Authenticate](examples/stytch-consumer-sessions-authenticate-example.json)
- [Consumer WebAuthn — Register Start](examples/stytch-consumer-webauthn-register-start-example.json)
- [Consumer Connected Apps — Create Client](examples/stytch-consumer-connected-apps-create-example.json)
- [Consumer Fraud — Fingerprint Lookup](examples/stytch-consumer-fingerprint-lookup-example.json)
- [Consumer Users — Create](examples/stytch-consumer-users-create-example.json)
- [B2B Organizations — Create](examples/stytch-b2b-organizations-create-example.json)
- [B2B Members — Create](examples/stytch-b2b-members-create-example.json)
- [B2B SSO — Create SAML Connection](examples/stytch-b2b-sso-saml-create-connection-example.json)
- [B2B Discovery — List Organizations](examples/stytch-b2b-discovery-organizations-example.json)
- [B2B Magic Links — Email Login or Signup](examples/stytch-b2b-magic-links-email-login-or-signup-example.json)
- [B2B Sessions — Authenticate](examples/stytch-b2b-sessions-authenticate-example.json)
- [B2B RBAC — Get Policy](examples/stytch-b2b-rbac-policy-get-example.json)
- [Management — Create Project](examples/stytch-management-create-project-example.json)
- [Management — Create Redirect URL](examples/stytch-management-create-redirect-url-example.json)

## SDKs & Tooling

| Language / Surface | Repo |
|---|---|
| Node.js | [stytch-node](https://github.com/stytchauth/stytch-node) |
| Python | [stytch-python](https://github.com/stytchauth/stytch-python) |
| Go | [stytch-go](https://github.com/stytchauth/stytch-go) |
| Ruby | [stytch-ruby](https://github.com/stytchauth/stytch-ruby) |
| Java / Kotlin | [stytch-java](https://github.com/stytchauth/stytch-java) |
| PHP | [stytch-php](https://github.com/stytchauth/stytch-php) |
| .NET | [stytch-dotnet](https://github.com/stytchauth/stytch-dotnet) |
| Rust | [stytch-rust](https://github.com/stytchauth/stytch-rust) |
| iOS | [stytch-ios](https://github.com/stytchauth/stytch-ios) |
| Android / Mobile | [stytch-android](https://github.com/stytchauth/stytch-android), [stytch-mobile](https://github.com/stytchauth/stytch-mobile) |
| Browser | [stytch-browser](https://github.com/stytchauth/stytch-browser) |
| CLI | [stytch-cli](https://github.com/stytchauth/stytch-cli) |
| Terraform | [terraform-provider-stytch](https://github.com/stytchauth/terraform-provider-stytch) |
| Management API SDKs | [stytch-management-node](https://github.com/stytchauth/stytch-management-node), [stytch-management-go](https://github.com/stytchauth/stytch-management-go), [stytch-management-python](https://github.com/stytchauth/stytch-management-python) |
| AI Agent detection | [is-agent](https://github.com/stytchauth/is-agent) |
| SAML hardening | [samlshield](https://github.com/stytchauth/samlshield) |
| MCP server demos | [mcp-stytch-consumer-todo-list](https://github.com/stytchauth/mcp-stytch-consumer-todo-list), [stytch-connected-apps-b2b-demo](https://github.com/stytchauth/stytch-connected-apps-b2b-demo), [mcp-stytch-b2b-okr-manager](https://github.com/stytchauth/mcp-stytch-b2b-okr-manager) |

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
