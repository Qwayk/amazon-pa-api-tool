# amazon-pa-api-tool (Amazon PA‑API v5)

Read-only CLI for the Amazon Product Advertising API (PA‑API v5).

## For non-technical users: Start here (no coding)

Start with these docs:

- Use cases (ideas + benefits): `docs/use_cases.md`
- Onboarding (setup + what to ask your agent): `docs/onboarding.md`
- Safety model (how we prevent mistakes): `docs/safety_model.md`

What you can ask an AI agent to do (examples):

- “Find 20 candidate products for ‘X’ and give me a shortlist with titles and images.”
- “Resolve these Amazon URLs into ASINs and build clean affiliate links.”
- “Create a batch job from my spreadsheet and produce a report of results.”

## Scope and safety (by design)

- This tool is **read-only** to Amazon APIs.
- `--apply` exists for consistency across tools but does not enable external writes here.

## For technical users: Start here (CLI)

Full references:
- `docs/quickstart.md`
- `docs/command_reference.md`

Minimal examples:

```bash
amazon-pa-api-tool --version
amazon-pa-api-tool auth check
amazon-pa-api-tool product search --query "test" --limit 1
```

## Proof pack (customer-ready)

- `docs/proof.md`
- `docs/references.md`
- `docs/api_coverage.md`
- `docs/examples/`

## Skills wrapper

If you use an agent runtime that supports “skills” (example: Codex), this tool ships a minimal safe wrapper:

- Skill: `skills/amazon-pa-api-safe-cli/SKILL.md`
- Skill docs: `docs/skills_wrappers.md`
