# First Call Guide

This guide helps you verify that your OriginStartAI key, base URL, and model are working before you build a larger integration.

## 1. Prepare Environment Variables

```bash
cp .env.example .env
```

Fill in:

```bash
ORIGINSTARTAI_API_KEY=your_api_key_here
ORIGINSTARTAI_BASE_URL=https://YOUR_PUBLIC_API_BASE_URL/v1
ORIGINSTARTAI_MODEL=YOUR_ENABLED_MODEL
```

## 2. Run Python

```bash
python examples/python/first_call.py
```

Expected result: a JSON response containing a model answer.

## 3. Run Node.js

```bash
node examples/node/first_call.mjs
```

Expected result: the same kind of chat completion response.

## 4. Next Step

Once the first call works, replace the sample prompt with a real product task:

- Summarize a support ticket.
- Draft a product description.
- Convert a user request into structured JSON.
- Generate a concise SEO outline.

For new accounts, check the console recharge page: recharge `$5` and get `$5` extra API credits.
