# `amazon-pa-api-tool` docs

Non-technical start here:
- `use_cases.md` (what you can do)
- `onboarding.md` (setup + what to ask your agent)
- `safety_model.md` (how we prevent mistakes)

Technical references:
- `quickstart.md` (commands)
- `command_reference.md` (commands)

Proof pack:
- `proof.md`
- `references.md`
- `api_coverage.md`
- `skills_wrappers.md`

Agent Skills:
- `skills_wrappers.md`
- Skill: `../skills/amazon-pa-api-safe-cli/SKILL.md`

Recommended workflows:

- Validate credentials: `amazon-pa-api-tool auth check`
- Find candidate products: `amazon-pa-api-tool product search --query "..." --limit 10`
- Fetch title + images for known ASINs: `amazon-pa-api-tool product get --asin ...`
- Build a clean affiliate link: `amazon-pa-api-tool link build --asin ...`

Notes:
- This tool intentionally does **not** return price/ratings by default (keep price checks on Amazon).
- `--include-raw` exists for research/debugging; default output stays small and stable for automation.
