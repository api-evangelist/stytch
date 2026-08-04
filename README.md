# Stytch (stytch)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Stytch is an authentication and identity infrastructure provider. Its Consumer and B2B APIs cover passwordless authentication (Magic Links, OTP, OAuth, WebAuthn / Passkeys, TOTP), enterprise SSO (SAML / OIDC) and SCIM, sessions, M2M client-credentials tokens, and Device Fingerprinting / fraud defense. Connected Apps lets a Stytch-secured product act as an OAuth 2.0 / OIDC Authorization Server for third-party integrations, desktop apps, AI agents, and MCP servers — a posture Stytch describes as "agent-ready". A separate Management API plus a Terraform provider handle workspace configuration as code.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/stytch/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/stytch/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Authentication
- Identity
- Passwordless
- Security
- B2B
- Connected Apps
- MCP
- AI Agents
- Developer Tools

## Timestamps

- **Created:** 2024-11-15
- **Modified:** 2026-05-22

## APIs

### Stytch Consumer Authentication API

Stytch's Consumer API for end-user authentication. Covers Magic Links, SMS / email / WhatsApp OTP, OAuth social login, Passwords, TOTP, WebAuthn / Passkeys, Crypto Wallets, Sessions, Users, plus the M2M (client credentials) surface, Connected Apps (OAuth provider for third-party tools, AI agents, and MCP servers), Fraud / Device Fingerprinting, Impersonation, IDP introspection, and Consumer RBAC.

- **Human URL:** [https://stytch.com/docs/api](https://stytch.com/docs/api)
- **Base URL:** `https://api.stytch.com`

#### Tags

- Authentication
- Passwordless
- Magic Links
- OTP
- OAuth
- WebAuthn
- Passkeys
- Consumer
- M2M
- Connected Apps
- Fraud

#### Properties

- [Documentation](https://stytch.com/docs/api)
- [API Reference](https://stytch.com/docs/api/reference/library/overview)
- [OpenAPI](openapi/stytch-consumer-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/stytch-consumer.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/stytch-consumer.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Open A P I Source](https://github.com/stytchauth/stytch-openapi)

### Stytch B2B Authentication API

Stytch's B2B API for multi-tenant SaaS authentication. Covers Organizations, Members, SSO (SAML and OIDC), Magic Links, OTP, OAuth, Discovery, Sessions, B2B RBAC, SCIM directory sync, TOTP, Recovery Codes, Passwords, Impersonation, and the B2B IDP surface used by Connected Apps.

- **Human URL:** [https://stytch.com/docs/b2b](https://stytch.com/docs/b2b)
- **Base URL:** `https://api.stytch.com/v1/b2b`

#### Tags

- Authentication
- B2B
- SSO
- SAML
- OIDC
- SCIM
- Multi-Tenant
- Organizations
- RBAC
- Connected Apps

#### Properties

- [Documentation](https://stytch.com/docs/b2b)
- [API Reference](https://stytch.com/docs/b2b/api/overview)
- [OpenAPI](openapi/stytch-b2b-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/stytch-b2b.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/stytch-b2b.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Open A P I Source](https://github.com/stytchauth/stytch-openapi)

### Stytch Management API

Stytch's Workspace Management API (management.stytch.com) for programmatic configuration — projects, environments, secrets, redirect URLs, allowed country codes, RBAC policies, email templates, JWT templates, event log streaming, public tokens, trusted token profiles, and Consumer / B2B SDK configuration. Backs the Terraform provider and the language-specific management SDKs.

- **Human URL:** [https://stytch.com/docs/workspace-management-api](https://stytch.com/docs/workspace-management-api)
- **Base URL:** `https://management.stytch.com`

#### Tags

- Management
- Configuration
- Projects
- Secrets
- RBAC
- SDKConfig

#### Properties

- [Documentation](https://stytch.com/docs/workspace-management-api)
- [OpenAPI](openapi/stytch-management-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/stytch-management.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/stytch-management.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Open A P I Source](https://github.com/stytchauth/stytch-management-openapi)
- [Terraform Provider](https://github.com/stytchauth/terraform-provider-stytch)
- [SDK](https://github.com/stytchauth/stytch-management-node)
- [SDK](https://github.com/stytchauth/stytch-management-go)
- [SDK](https://github.com/stytchauth/stytch-management-python)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [Website](https://stytch.com)
- [Documentation](https://stytch.com/docs)
- [API Reference](https://stytch.com/docs/api)
- [Sign Up](https://app.stytch.com/register)
- [Portal](https://app.stytch.com)
- [Authentication](https://stytch.com/docs/guides/authentication)
- [Sessions](https://stytch.com/docs/guides/sessions)
- [Connected Apps](https://stytch.com/docs/guides/connected-apps/overview)
- [M C P Server](https://github.com/stytchauth/mcp-stytch-consumer-todo-list)
- [A I Agent Detection](https://github.com/stytchauth/is-agent)
- [S D Ks](https://stytch.com/docs/sdks)
- [Pricing](https://stytch.com/pricing)
- [Privacy Policy](https://stytch.com/privacy)
- [Terms of Service](https://stytch.com/terms)
- [Webhooks](https://stytch.com/docs/guides/webhooks)
- [GitHub Organization](https://github.com/stytchauth)
- [Postman Workspace](https://www.postman.com/stytch/stytch-public-workspace/overview)
- [LinkedIn](https://www.linkedin.com/company/stytch)
- [Node.js  S D K](https://github.com/stytchauth/stytch-node)
- [Python  S D K](https://github.com/stytchauth/stytch-python)
- [Java  S D K](https://github.com/stytchauth/stytch-java)
- [Go  S D K](https://github.com/stytchauth/stytch-go)
- [Ruby  S D K](https://github.com/stytchauth/stytch-ruby)
- [P H P  S D K](https://github.com/stytchauth/stytch-php)
- [. N E T  S D K](https://github.com/stytchauth/stytch-dotnet)
- [Rust  S D K](https://github.com/stytchauth/stytch-rust)
- [i O S  S D K](https://github.com/stytchauth/stytch-ios)
- [Android  S D K](https://github.com/stytchauth/stytch-android)
- [Browser  S D K](https://github.com/stytchauth/stytch-browser)
- [Mobile  S D K](https://github.com/stytchauth/stytch-mobile)
- [C L I](https://github.com/stytchauth/stytch-cli)
- [Terraform Provider](https://github.com/stytchauth/terraform-provider-stytch)
- [Management S D K](https://github.com/stytchauth/stytch-management-node)
- [O S S  Library](https://github.com/stytchauth/samlshield)
- [Status Page](https://status.stytch.com)
- [Blog](https://stytch.com/blog)
- [Spectral  Rules](rules/stytch-rules.yml)
- [Vocabulary](vocabulary/stytch-vocabulary.yml)
- [J S O N  Schema](json-schema/stytch-user-schema.json)
- [J S O N  Schema](json-schema/stytch-organization-schema.json)
- [J S O N  Schema](json-schema/stytch-member-schema.json)
- [J S O N  Schema](json-schema/stytch-connected-app-schema.json)
- [J S O N  Schema](json-schema/stytch-m2m-client-schema.json)
- [J S O N  Structure](json-structure/stytch-session-structure.json)
- [J S O N  Structure](json-structure/stytch-connected-app-structure.json)
- [J S O N- L D  Context](json-ld/stytch-context.jsonld)
- [Example](examples/stytch-send-magic-link-example.json)
- [Example](examples/stytch-create-organization-example.json)
- [Example](examples/stytch-consumer-magic-links-login-or-create-example.json)
- [Example](examples/stytch-consumer-otps-sms-send-example.json)
- [Example](examples/stytch-consumer-oauth-authenticate-example.json)
- [Example](examples/stytch-consumer-sessions-authenticate-example.json)
- [Example](examples/stytch-consumer-webauthn-register-start-example.json)
- [Example](examples/stytch-consumer-connected-apps-create-example.json)
- [Example](examples/stytch-consumer-fingerprint-lookup-example.json)
- [Example](examples/stytch-consumer-users-create-example.json)
- [Example](examples/stytch-b2b-organizations-create-example.json)
- [Example](examples/stytch-b2b-members-create-example.json)
- [Example](examples/stytch-b2b-sso-saml-create-connection-example.json)
- [Example](examples/stytch-b2b-discovery-organizations-example.json)
- [Example](examples/stytch-b2b-magic-links-email-login-or-signup-example.json)
- [Example](examples/stytch-b2b-sessions-authenticate-example.json)
- [Example](examples/stytch-b2b-rbac-policy-get-example.json)
- [Example](examples/stytch-management-create-project-example.json)
- [Example](examples/stytch-management-create-redirect-url-example.json)
- [Plans](plans/stytch-plans-pricing.yml)
- [Rate Limits](rate-limits/stytch-rate-limits.yml)
- [Fin Ops](finops/stytch-finops.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
