---
name: mailsenpai-suppression-add-remove
description: Add an address or domain to the suppression list and then remove it when no longer needed.
api: openapi/mailsenpai-openapi.json
operations:
- sopprimi
- riammetti
- soppressi
generated: '2026-10-12'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/mailsenpai-openapi.json ; every operationId checked against the contract
---

# mailsenpai-suppression-add-remove

Add an address or domain to the suppression list and then remove it when no longer needed.

## Steps

1. 1. Call `sopprimi` with the required body fields `address` (or `domain`) and optional `reason`.
2. 2. Call `riammetti` with the identifier field `id` of the entry you added.
3. 3. Optionally call `soppressi` to verify the current suppression list.

## Rules

- Auth: Include the `Authorization: Bearer <token>` header using the `chiaveBearer` scheme.
- Idempotency: The `sopprimi` operation is not idempotent; avoid duplicate submissions.
- Errors: The API returns standard HTTP error codes (e.g., 400 for bad request, 401 for unauthorized, 404 for not found).
