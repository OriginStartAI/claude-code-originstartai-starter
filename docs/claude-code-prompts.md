# Claude Code Task Prompts

Use these prompts after the first API call works.

## Add Retry Logic

```text
Add retry handling to the OriginStartAI request helper. Keep the example dependency-free and print clear errors for 401, model not found, insufficient credits, and timeout.
```

## Add a Product Workflow

```text
Create a new example that turns a customer support ticket into a short, friendly reply using the existing OriginStartAI environment variables.
```

## Add Structured Output

```text
Create a JSON-only example that extracts action items from a user request. Validate that the response parses as JSON before printing it.
```

## Prepare for Production

```text
Split the example into a reusable client module and a CLI entrypoint. Keep secrets in environment variables and add a README section explaining deployment.
```
