# Resume Editor Agent

This repository is focused on the Resume Editor Agent setup: custom agent instructions, skills, and a safe example LaTeX template.

Private resume source/output files are intentionally ignored.

## Included in this repository

- `.github/agents/` - custom agent definitions
- `.github/instructions/` - workflow and usage instructions
- `.github/skills/` - reusable skills (LaTeX, ATS checker, Canva guidance)
- `examples/resume_template.tex` - sample resume format with placeholder data only

## Intentionally ignored

- All `.pdf` files
- All `.tex` files except the safe example template
- LaTeX build artifacts (`.aux`, `.log`, etc.)

See `.gitignore` for the full ignore policy.

## Example usage

Compile the safe example template:

```sh
cd /Users/ishritthakur/First-Agent
/opt/homebrew/bin/tectonic examples/resume_template.tex
```

## Notes

- Use your local private resume files outside version control.
- Keep agent/skill updates in `.github/` tracked and reviewable.
