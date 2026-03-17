# Use cases (what you can do)

This page is for non-technical users. It shows the kinds of outcomes you can ask an AI agent to achieve using `amazon-pa-api-tool`.

If you want the exact commands, see `docs/quickstart.md` and `docs/command_reference.md`.

## Why this is powerful (vs typical no‑code automation)

No‑code tools can store affiliate links. This tool is built for repeatable product research workflows:

- Fast bulk searches and retrieval (titles, images, key metadata)
- Deterministic outputs for automation (stable JSON shapes)
- Batch jobs from spreadsheets

## Common use cases (examples)

- “Find 30 products for ‘X’ and shortlist the best 10 with images.”
- “Fetch product details for these ASINs and export a clean JSON/CSV report.”
- “Resolve a list of Amazon URLs into ASINs and build clean affiliate links.”
- “Run a batch job from a CSV and give me a receipt of what succeeded/failed.”

## What you’ll see from the agent (trust + safety)

This tool is read-only. The agent should still provide:

- A short description of what was queried
- Where outputs were saved (if exported)
- Any errors/refusals (for invalid URLs, missing credentials, etc.)

