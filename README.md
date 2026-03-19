# Amazon PA-API tool for AI agents

This is a public Qwayk proof repo.

It gives AI agents a safe way to work with the Amazon Product Advertising API (PA-API v5).
In this case, "safe" is simple because the tool is read-only.

## What this tool is for

Use this when you want an agent to help with Amazon product data work like:
- product research
- ASIN lookup
- affiliate link cleanup
- batch reporting

## Why this repo is public

This repo shows the Qwayk model in the simplest possible way:
- real API work
- local-first usage
- machine-friendly output
- no external writes

It is a good first example because there is no risk of changing Amazon data.

## For non-technical users

Start here:
- `docs/use_cases.md`
- `docs/onboarding.md`
- `docs/safety_model.md`

Example things to ask your agent:
- “Find product ideas for this keyword and give me a shortlist.”
- “Turn these Amazon URLs into ASINs.”
- “Build clean affiliate links from this list.”

## For technical users

Start here:
- `docs/quickstart.md`
- `docs/command_reference.md`

Minimal examples:

```bash
amazon-pa-api-tool --version
amazon-pa-api-tool auth check
amazon-pa-api-tool product search --query "test" --limit 1
```

## Skills and wrappers

This tool ships with a skill wrapper for agent runtimes that support skills:
- `skills/amazon-pa-api-safe-cli/SKILL.md`
- `docs/skills_wrappers.md`

## Qwayk

- Start here: `https://github.com/Qwayk/start-here`
- Sponsor Qwayk: `https://github.com/sponsors/Qwayk`
