# Programmatic API Onboarding — Stytch

A single-file, zero-dependency Node.js (18+) CLI that reproduces SoundCloud's
`sc-api-auth.mjs` pattern for Stytch: register an application / obtain credentials
programmatically instead of clicking through a dashboard, so agents and developers
can onboard at the command line.

- Script: [`stytch-api-auth.mjs`](stytch-api-auth.mjs)
- Run `node stytch-api-auth.mjs --help` for usage and the required environment variables.
- Story / rationale: https://apievangelist.com/2026/08/05/stytch-built-self-serve-onboarding/

Part of the API Evangelist "Programmatic API Onboarding for the Agentic Moment" series.
