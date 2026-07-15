# Troubleshooting

## `401 Unauthorized`

Check:

- `ORIGINSTARTAI_API_KEY` is set.
- The key has not been copied with extra spaces.
- The key belongs to the account you are testing.

## `model not found`

Check:

- `ORIGINSTARTAI_MODEL` is enabled for your account.
- The model name is copied exactly from the console.
- Your account has access to the selected model group.

## `insufficient credits`

Recharge in the OriginStartAI console. New users can recharge `$5` and get `$5` extra API credits.

## Slow Responses

Try:

- Shorter prompts.
- Smaller context windows.
- Retrying transient failures.
- Testing another enabled model.

## Network Errors

Check:

- `ORIGINSTARTAI_BASE_URL` includes `/v1`.
- Your firewall or proxy allows outbound HTTPS traffic.
- The endpoint is reachable from your server or local network.
