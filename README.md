# Claude Code OriginStartAI Starter

Run your first OriginStartAI API call from a Claude Code style workflow in minutes.

## Why This Exists

This starter is for developers who want an OpenAI-compatible API endpoint that is easy to test from terminal tools, scripts, and Claude Code related workflows.

## Quick Start

1. Get your API key from https://originstartai.com
2. Copy `.env.example` to `.env`
3. Set `ORIGINSTARTAI_API_KEY`
4. Run the curl, Python, or Node.js example

New user bonus: recharge `$5` and get `$5` extra API credits.

## curl

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

## Python

```bash
python examples/python/first_call.py
```

## Node.js

```bash
node examples/node/first_call.mjs
```

## Environment

```bash
ORIGINSTARTAI_API_KEY=your_api_key_here
ORIGINSTARTAI_BASE_URL=https://YOUR_7016_API_BASE_URL/v1
ORIGINSTARTAI_MODEL=YOUR_DEFAULT_MODEL
```

## Troubleshooting

- `401 Unauthorized`: check whether your API key is correct.
- `insufficient credits`: recharge in the OriginStartAI console.
- `model not found`: check whether the selected model is enabled for your account.
- `timeout`: retry later or reduce the prompt size.

## Links

- Website: https://originstartai.com
- Support: support@originstartai.com

