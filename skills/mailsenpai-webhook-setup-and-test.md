---
name: mailsenpai-webhook-setup-and-test
description: Configure a webhook, send a test event, and verify the webhook settings.
api: openapi/mailsenpai-openapi.json
operations:
- webhookImposta
- webhookProva
- webhookLeggi
generated: '2026-10-12'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/mailsenpai-openapi.json ; every operationId checked against the contract
---

# mailsenpai-webhook-setup-and-test

Configure a webhook, send a test event, and verify the webhook settings.

## Steps

1. 1. Call `webhookImposta` with the request body fields required to set or disable the webhook.
2. 2. Call `webhookProva` with any required payload to trigger an immediate test event.
3. 3. Call `webhookLeggi` to retrieve the current webhook configuration.

## Rules

- Include the `Authorization: Bearer <token>` header as defined by the `chiaveBearer` scheme.
- All requests are sent to the base URL `https://app.mailsenpai.com/relay/v1`.
