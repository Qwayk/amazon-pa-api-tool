# Agent Skills wrappers

This tool ships a minimal “Agent Skills” wrapper intended for deterministic, safe tool use inside agent runtimes (example: Codex skills).

The wrapper is a small instruction file that tells an agent:
- which CLI to call,
- which safety rules to follow,
- when to refuse,
- and how to avoid accidental large/batch requests.

## Canonical skill location

- Skill: `skills/amazon-pa-api-safe-cli/SKILL.md`
- Scope rules: `skills/AGENTS.md`

## Installing the skill (Codex)

Copy (or symlink) the skill folder into your Codex skills directory so the runtime can load it.

Example layout:
- `~/.codex/skills/amazon-pa-api-safe-cli/SKILL.md`

## Safety notes for this tool

`amazon-pa-api-tool` is **read-only** (no external writes), but it can still create problems if you accidentally trigger many API requests (quota/cost).

Rules the skill enforces:
- Always run with `--output json`.
- Never expose secrets.
- Require `--yes` when a command will expand into multiple PA‑API requests (more than 10 IDs, or `--max-requests` > 1).
- Start small: run a sample query/ASIN first before large batches.

## Example commands (dummy values)

Validate configuration:

```bash
amazon-pa-api-tool --output json auth check
```

Search for products:

```bash
amazon-pa-api-tool --output json product search --query "wireless earbuds" --limit 3
```

Fetch multiple items (requires `--yes` if you pass more than 10 ASINs or allow multiple requests):

```bash
amazon-pa-api-tool --output json product get --asin B000000000 --asin B000000001
```

## Plan/receipt artifacts (optional, recommended)

This tool does not currently write plan/receipt files automatically, but you can still capture “proof artifacts” by saving:
- the exact command you ran, and
- the resulting JSON output.

Documentation examples of plan/receipt shapes:
- `docs/examples/plan.example.json`
- `docs/examples/receipt.example.json`
