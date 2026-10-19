---
name: knoxcall-signup
description: Create a new account via headless signup and then claim the starter credentials.
api: openapi/knoxcall-openapi.json
operations:
- createAccount
- claimSignup
generated: '2026-10-18'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/knoxcall-openapi.json ; every operationId checked against the contract
---

# knoxcall-signup

Create a new account via headless signup and then claim the starter credentials.

## Steps

1. 1. Call `createAccount` with the required request body fields for account creation.
2. 2. Call `claimSignup` with the signup token returned from `createAccount` to collect starter credentials.

## Rules

- Auth: Include the API key in header `x-api-key` (ApiKeyAuth) or use Bearer token as required by the endpoint.
- Rate limit: Maximum 100 requests per minute; exceeding returns HTTP 429.
