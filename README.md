# Stytch (stytch)
Stytch provides secure and seamless authentication solutions for businesses. Their platform enables passwordless authentication via magic links, OTP, OAuth, WebAuthn, and biometrics for consumer apps, plus B2B multi-tenant authentication with SSO, organizations, and role-based access control for SaaS platforms.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/stytch/refs/heads/main/apis.yml)

## Scope

- **Type:** Contract
- **Position:** Consuming
- **Access:** 3rd-Party

## Tags:

 - Authentication, Identity, Passwordless, Security, Developer Tools

## Timestamps

- **Created:** 2024-11-15
- **Modified:** 2026-05-02

## APIs

### Stytch Consumer Authentication API
Passwordless and password-based authentication for consumer applications. Supports magic links, SMS/email OTP, OAuth social login, TOTP (authenticator apps), WebAuthn (passkeys/biometrics), passwords, and session management.

#### Tags:
 - Authentication, Passwordless, Magic Links, OTP, Consumer

#### Properties

- [Documentation](https://stytch.com/docs/api)
- [API Reference](https://stytch.com/docs/api/reference/library/overview)
- [OpenAPI](openapi/stytch-consumer-openapi.yml)

---

### Stytch B2B Authentication API
Multi-tenant authentication for SaaS applications. Supports organizations (tenants), members, SSO via SAML/OIDC, magic links, OTP, OAuth, organization discovery, and B2B session management.

#### Tags:
 - Authentication, B2B, SSO, Multi-Tenant, Organizations

#### Properties

- [Documentation](https://stytch.com/docs/b2b)
- [API Reference](https://stytch.com/docs/b2b/api/overview)
- [OpenAPI](openapi/stytch-b2b-openapi.yml)

---

## Common Properties

- [Website](https://stytch.com)
- [Documentation](https://stytch.com/docs)
- [Sign Up](https://app.stytch.com/register)
- [Portal](https://app.stytch.com)
- [GitHub](https://github.com/stytchauth)
- [Postman Workspace](https://www.postman.com/stytch/stytch-public-workspace/overview)
- [Status](https://status.stytch.com)
- [Pricing](https://stytch.com/pricing)
- [Spectral Rules](rules/stytch-rules.yml)
- [Vocabulary](vocabulary/stytch-vocabulary.yml)

## Capabilities

### Workflow Capabilities

| Capability | Description |
|---|---|
| [Passwordless Authentication](capabilities/passwordless-authentication.yaml) | Consumer passwordless auth — Magic Links, OTP, Session Management |
| [B2B Identity Management](capabilities/b2b-identity-management.yaml) | B2B auth — Organizations, Members, SSO, Discovery |

### Shared API Definitions

| API | File |
|---|---|
| Consumer Auth | [shared/consumer-auth.yaml](capabilities/shared/consumer-auth.yaml) |
| B2B Auth | [shared/b2b-auth.yaml](capabilities/shared/b2b-auth.yaml) |

## JSON Schemas

- [stytch-user-schema.json](json-schema/stytch-user-schema.json) — Consumer User
- [stytch-organization-schema.json](json-schema/stytch-organization-schema.json) — B2B Organization

## JSON Structures

- [stytch-session-structure.json](json-structure/stytch-session-structure.json) — Session object structure

## JSON-LD

- [stytch-context.jsonld](json-ld/stytch-context.jsonld)

## Examples

- [Send Magic Link](examples/stytch-send-magic-link-example.json)
- [Create B2B Organization](examples/stytch-create-organization-example.json)

## SDKs

- [Node.js](https://github.com/stytchauth/stytch-node)
- [Python](https://github.com/stytchauth/stytch-python)
- [Java](https://github.com/stytchauth/stytch-java)
- [Go](https://github.com/stytchauth/stytch-go)
- [Ruby](https://github.com/stytchauth/stytch-ruby)
- [PHP](https://github.com/stytchauth/stytch-php)

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
