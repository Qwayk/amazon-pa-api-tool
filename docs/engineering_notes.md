# Engineering notes

Last updated (UTC): 2026-01-22

## Notes

- This tool is intentionally **read-only**; `--apply` exists only to match the repo-wide CLI flag standard.
- `--output json` enforces a strict contract: exactly one JSON object on stdout for successes and errors, including parse/usage errors (argparse exits are intercepted).

