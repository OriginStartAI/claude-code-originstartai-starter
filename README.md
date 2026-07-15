# Claude Code OriginStartAI Starter

Run your first OriginStartAI API call from a Claude Code style workflow in minutes.

This repo is designed for developers who want a small, copyable, OpenAI-compatible starter they can test from a terminal, adapt inside Claude Code, and then move into a real product workflow.

## Fast Path

1. Create an account at https://originstartai.com?utm_source=github&utm_medium=repo&utm_campaign=claude_code_starter
2. Get an API key from the OriginStartAI console.
3. Copy `.env.example` to `.env`.
4. Set `ORIGINSTARTAI_API_KEY`, `ORIGINSTARTAI_BASE_URL`, and `ORIGINSTARTAI_MODEL`.
5. Run one of the examples below.

New user bonus: recharge `$5` and get `$5` extra API credits.

## First API Call

```bash
python examples/python/first_call.py
```

```bash
node examples/node/first_call.mjs
```

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

## Claude Code Workflow

Use this starter as a minimal project that Claude Code can inspect and modify:

```text
1. Run the first call.
2. Ask Claude Code to add your product-specific prompt.
3. Add a small test payload in `examples/`.
4. Move stable code into your app.
```

Recommended prompts:

```text
Add a product support reply example using the existing OriginStartAI client style.
```

```text
Convert this single API call into a reusable helper with retries and clear error messages.
```

## Environment

```bash
ORIGINSTARTAI_API_KEY=your_api_key_here
ORIGINSTARTAI_BASE_URL=https://YOUR_PUBLIC_API_BASE_URL/v1
ORIGINSTARTAI_MODEL=YOUR_ENABLED_MODEL
```

## Docs

- [First call guide](docs/first-call.md)
- [Troubleshooting](docs/troubleshooting.md)
- [Recharge and credits](docs/recharge-and-credits.md)
- [Claude Code task prompts](docs/claude-code-prompts.md)

## Troubleshooting

- `401 Unauthorized`: check whether your API key is correct.
- `insufficient credits`: recharge in the OriginStartAI console.
- `model not found`: check whether the selected model is enabled for your account.
- `timeout`: retry later, reduce the prompt size, or add retry logic.

## Links

- Website: https://originstartai.com?utm_source=github&utm_medium=repo&utm_campaign=claude_code_starter
- Support: support@originstartai.com
