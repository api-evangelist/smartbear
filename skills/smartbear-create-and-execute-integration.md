---
name: smartbear-create-and-execute-integration
description: Create a new API integration and then execute it.
api: openapi/smartbear-integrations-api-openapi.yml
operations:
- createApiIntegration
- executeApiIntegration
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/smartbear-integrations-api-openapi.yml ; every operationId checked against the contract
---

# smartbear-create-and-execute-integration

Create a new API integration and then execute it.

## Steps

1. 1. Use `createApiIntegration` with required body fields and the `Authorization` header.
2. 2. Use `executeApiIntegration` with path parameters `owner`, `api`, `version`, `integrationId` and the `Authorization` header.

## Rules

- Auth: Include an `Authorization` header with the API key (ApiKeyAuth).
- Idempotency: `createApiIntegration` is not idempotent; repeat calls will create duplicate integrations.
- Errors: The API returns standard HTTP error codes; on rate‑limit exhaustion there is no specific limit response.
