---
name: mailsenpai-website-forms-submit-and-retrieve
description: Submit a website form and then retrieve its submission details.
api: openapi/mailsenpai-openapi.json
operations:
- moduloInvia
- moduloInfo
generated: '2026-10-12'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/mailsenpai-openapi.json ; every operationId checked against the contract
---

# mailsenpai-website-forms-submit-and-retrieve

Submit a website form and then retrieve its submission details.

## Steps

1. 1. Use `moduloInvia` with the required path parameter `codice` and the form payload in the request body.
2. 2. Use `moduloInfo` with the same `codice` path parameter to get the reminder of how to use the address.

## Rules

- Auth: Include the `Authorization: Bearer <token>` header as defined by the `chiaveBearer` scheme.
- All requests are sent to the base URL `https://app.mailsenpai.com/relay/v1`.
