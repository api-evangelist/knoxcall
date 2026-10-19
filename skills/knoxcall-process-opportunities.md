---
name: knoxcall-process-opportunities
description: List promotion opportunities and either accept or dismiss a selected opportunity.
api: openapi/knoxcall-openapi.json
operations:
- listOpportunities
- acceptOpportunity
- dismissOpportunity
generated: '2026-10-18'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/knoxcall-openapi.json ; every operationId checked against the contract
---

# knoxcall-process-opportunities

List promotion opportunities and either accept or dismiss a selected opportunity.

## Steps

1. 1. Call `listOpportunities` – no request body; include authentication header (e.g., `x-api-key` or `Authorization`).
2. 2. Choose an opportunity ID from the response.
3. 3. Call `acceptOpportunity` – path parameter `id` required; include authentication header.
4. 4. (Optional) Call `dismissOpportunity` – path parameter `id` required; include authentication header.

## Rules

- Authentication: provide either `x-api-key` header (ApiKeyAuth) or `Authorization` header (BearerAuth, CapabilityTokenAuth, OAuth2, PhantomToken).
- Rate limiting: maximum 100 requests per minute; exceeding returns HTTP 429.
