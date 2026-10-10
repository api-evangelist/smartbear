---
name: smartbear-get-api-definition
description: Retrieve the full definition of a specific API version for a given owner.
api: openapi/smartbear-apis-api-openapi.yml
operations:
- getOwnerApis
- getApiVersions
- getDefinition
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/smartbear-apis-api-openapi.yml ; every operationId checked against the contract
---

# smartbear-get-api-definition

Retrieve the full definition of a specific API version for a given owner.

## Steps

1. 1. Call `getOwnerApis` with the `owner` path parameter to list the APIs owned by the user.
2. 2. Call `getApiVersions` with `owner` and `api` path parameters to list available versions of the selected API.
3. 3. Call `getDefinition` with `owner`, `api`, and `version` path parameters to obtain the API definition.

## Rules

- Authentication: Include an `Authorization` header with the API key (ApiKeyAuth).
- Idempotency: GET operations are safe and can be retried without side effects.
- Errors: The API returns standard HTTP error codes; on rate‑limit exhaustion no specific status code is defined.
