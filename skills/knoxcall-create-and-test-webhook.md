---
name: knoxcall-create-and-test-webhook
description: Create a new webhook and send a test delivery to verify it.
api: openapi/knoxcall-openapi.json
operations:
- createWebhook
- testWebhook
generated: '2026-10-18'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/knoxcall-openapi.json ; every operationId checked against the contract
---

# knoxcall-create-and-test-webhook

Create a new webhook and send a test delivery to verify it.

## Steps

1. 1. `createWebhook` – include required body fields for the webhook definition and the authentication header `x-api-key` (or `Authorization` for Bearer/OAuth2).
2. 2. `testWebhook` – provide the webhook `id` returned from step 1 and include the authentication header `x-api-key` (or `Authorization`).

## Rules

- Auth: Provide an API key in header `x-api-key` or a Bearer/OAuth2 token in header `Authorization`.
- Rate limit: 100 requests per minute; exceeding returns HTTP 429.
