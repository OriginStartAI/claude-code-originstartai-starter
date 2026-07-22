# Claude Code OriginStartAI Starter

Run a first OriginStartAI OpenAI-compatible API call from a Claude Code workflow, then turn the working call into product code.

This starter is for terminal-first developers who want a tiny repo Claude Code can inspect, modify, and extend without pulling in a heavy SDK or framework.

## 30-Second First Call

1. Create an account: https://originstartai.com?utm_source=github&utm_medium=repo&utm_campaign=claude_code_starter
2. Create an API key in the OriginStartAI console.
3. Copy `.env.example` to `.env`.
4. Set `ORIGINSTARTAI_API_KEY`, `ORIGINSTARTAI_BASE_URL`, and `ORIGINSTARTAI_MODEL`.
5. Run Python or Node.js:

```bash
python examples/python/first_call.py
```

```bash
node examples/node/first_call.mjs
```

New user bonus: after your first call works, recharge `$5` and get `$5` extra API credits to test a real workflow.

## Copyable curl Check

Use curl first when you only want to confirm that the API key, base URL, and model are valid:

```bash
curl "$ORIGINSTARTAI_BASE_URL/chat/completions" \
  -H "Authorization: Bearer $ORIGINSTARTAI_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "'"$ORIGINSTARTAI_MODEL"'",
    "messages": [
      {"role": "user", "content": "Say hello from OriginStartAI"}
    ]
  }'
```

## Why Developers Use This

- Claude Code friendly project layout.
- OpenAI-compatible request shape.
- Python and Node.js first-call examples.
- Minimal files that are easy to copy into an existing app.
- Clear next step from first call to a small paid production-style test.

## Claude Code Workflow

Open this repo in Claude Code and use one of these prompts after the first call succeeds:

```text
Add a product support reply example using the existing OriginStartAI client style.
```

```text
Convert this single API call into a reusable helper with retries and clear error messages.
```

```text
Add a streaming example that prints tokens as they arrive and handles timeout errors.
```

## If The First Call Fails

| Symptom | Check |
| --- | --- |
| `401 Unauthorized` | Confirm the API key in `.env` is current and has no extra spaces. |
| `insufficient credits` | Recharge in the OriginStartAI console, then retry the same command. |
| `model not found` | Copy the enabled model name from the console into `ORIGINSTARTAI_MODEL`. |
| `timeout` | Retry with a shorter prompt, then add retry and timeout handling before production use. |

## Environment

```bash
ORIGINSTARTAI_API_KEY=your_api_key_here
ORIGINSTARTAI_BASE_URL=https://YOUR_PUBLIC_API_BASE_URL/v1
ORIGINSTARTAI_MODEL=YOUR_ENABLED_MODEL
```

Do not commit `.env` or real API keys.

## Production Trust Checks

After the first call works, use the companion trust assets before moving a coding workflow into production:

- Estimate monthly spend with [`ai-api-cost-calculator`](https://github.com/OriginStartAI/ai-api-cost-calculator).
- Measure latency and success rate with [`ai-gateway-benchmark`](https://github.com/OriginStartAI/ai-gateway-benchmark).
- Add a lightweight health check with [`originstart-status-examples`](https://github.com/OriginStartAI/originstart-status-examples).

This path keeps the workflow practical: first call, cost estimate, benchmark, health check, then production usage.

## Docs

- [First call guide](docs/first-call.md)
- [Troubleshooting](docs/troubleshooting.md)
- [Recharge and credits](docs/recharge-and-credits.md)
- [Claude Code task prompts](docs/claude-code-prompts.md)

## Search Topics

- Claude Code API starter.
- OpenAI-compatible API starter.
- AI API first call.
- Chat completions from terminal.
- LLM workflow starter.

## Links

- Website: https://originstartai.com?utm_source=github&utm_medium=repo&utm_campaign=claude_code_starter
- Support: support@originstartai.com
