# First-Agent Resume Toolkit

This repository contains a resume conversion and update workflow for LaTeX and ATS-friendly resume content, plus custom GitHub Agent skill documentation.

## Contents

- `CV-1_copy_from_pdf.tex` — LaTeX resume source generated from the original PDF and updated for AI engineering.
- `CV-1_copy_from_pdf.pdf` — compiled PDF output from the LaTeX source.
- `CV-1 copy.pdf` — original source resume PDF.
- `.github/skills/latex-documents/` — skill documentation and templates for LaTeX resume authoring.
- `.github/skills/ats-checker/` — ATS resume analysis skill documentation.

## Usage

1. Edit `CV-1_copy_from_pdf.tex` to update resume content.
2. Compile with a LaTeX engine such as `tectonic`:
   ```sh
   cd /Users/ishritthakur/First-Agent
   /opt/homebrew/bin/tectonic CV-1_copy_from_pdf.tex
   ```
3. Review the generated `CV-1_copy_from_pdf.pdf`.

## Notes

- The current resume has been optimized for AI engineering roles.
- The ATS checker skill is documented under `.github/skills/ats-checker/SKILL.md`.
- The LaTeX resume workflow and templates are in `.github/skills/latex-documents/`.

## Project Goals

- Maintain a clean LaTeX resume source for iterative updates.
- Support ATS-focused resume analysis and keyword optimization.
- Preserve versioned output PDFs for review and comparison.
