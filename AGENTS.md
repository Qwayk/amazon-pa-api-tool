# qwayk-amazon-paapi-v5-safe-agent-cli — agent instructions

Scope: this folder.

## Safety + intent

- This tool is **read-only** against Amazon PA-API v5 (no external writes).
- Never print or commit secrets (API keys, tokens, `.env` contents, Authorization headers).
- Keep changes minimal and scoped to this tool folder.

## Output contract

- `--output json` must print **exactly one JSON object** to stdout on success and on errors (including parse/usage errors).
- `--version` must be machine-readable in `--output json` and must not require config/env.

## Skills wrapper (planned)

- Canonical location: `skills/amazon-pa-api-safe-cli/SKILL.md`
- Add `docs/skills_wrappers.md` when the wrapper ships and keep it in sync with CLI changes.

## Validation

## Python version

- This tool requires **Python 3.12+** (`requires-python = ">=3.12"` in `pyproject.toml`).

Preferred (isolated venv):
- `python3 -m venv .venv`
- `.venv/bin/python -m pip install -e .`
- `.venv/bin/python -m unittest -q`

Quick (Python 3.12+ already active):
- `python3 -m unittest -q`

## Agent Skills wrapper

This tool ships a skill wrapper under:
- `skills/AGENTS.md`
- `skills/amazon-pa-api-safe-cli/SKILL.md`

Also see: `docs/skills_wrappers.md`.
