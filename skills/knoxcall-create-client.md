---
name: knoxcall-create-client
description: Create a new client and retrieve its details.
api: openapi/knoxcall-openapi.json
operations:
- createClient
- getClient
generated: '2026-10-18'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/knoxcall-openapi.json ; every operationId checked against the contract
---

# knoxcall-create-client

Create a new client and retrieve its details.

## Steps

1. 1. Use `createClient` with body fields as defined in the contract.
2. 2. Use `getClient` with path parameter `id` returned from the create step.

## Rules

- Auth: include the API key in header `x-api-key` (ApiKeyAuth) or a Bearer token (BearerAuth).
- Rate limit: maximum 100 requests per minute; HTTP 429 returned when exceeded.
