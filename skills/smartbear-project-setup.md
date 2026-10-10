---
name: smartbear-project-setup
description: Create a new project for an owner and attach APIs and domains to it.
api: openapi/smartbear-projects-api-openapi.yml
operations:
- createProject
- addApiToProject
- addDomainToProject
- getProject
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/smartbear-projects-api-openapi.yml ; every operationId checked against the contract
---

# smartbear-project-setup

Create a new project for an owner and attach APIs and domains to it.

## Steps

1. 1. `createProject` – send a POST to `/projects/{owner}` with the `Authorization` header (ApiKey) and a request body containing the project definition.
2. 2. `addApiToProject` – send a POST to `/projects/{owner}/{project}/apis` with the `Authorization` header and a body specifying the API to add.
3. 3. `addDomainToProject` – send a POST to `/projects/{owner}/{project}/domains` with the `Authorization` header and a body specifying the domain to add.
4. 4. `getProject` – send a GET to `/projects/{owner}/{project}` with the `Authorization` header to verify the project and its attached resources.

## Rules

- Include the `Authorization` header containing the API key for every request (ApiKeyAuth).
