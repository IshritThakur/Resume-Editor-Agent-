---
name: latex-documents
description: 'Create, edit, and troubleshoot LaTeX documents. Use for: resume writing, formatting complex documents, managing packages, fixing compilation errors, styling text, organizing document structure.'
argument-hint: 'Describe what you want to create or fix (e.g., "create a professional resume template", "fix undefined control sequence error")'
user-invocable: true
---

# LaTeX Documents Skill

Master LaTeX document creation and editing for resumes, reports, articles, and professional documents.

## When to Use

- Creating a professional resume with consistent styling
- Building formatted documents (reports, papers, proposals)
- Troubleshooting LaTeX compilation errors
- Organizing complex document structure with sections and subsections
- Managing packages and dependencies
- Styling text, colors, fonts, and spacing
- Converting between document formats or templates

## Key Capabilities

This skill provides:
1. **Resume Templates** - Professional, ATS-friendly resume structures in LaTeX
2. **Packages Reference** - Common packages and their use cases
3. **Formatting Examples** - Code snippets for styling and layout
4. **Troubleshooting Guide** - Solutions for common LaTeX errors
5. **Style Guide** - Best practices for professional documents

## Procedure

### Creating a Document
1. Choose a template from [resume templates](./assets/templates.tex) or start from scratch
2. Identify your document class (`article`, `resume`, `report`)
3. Load necessary packages from [packages reference](./references/packages.md)
4. Structure your content using sections and appropriate environments
5. Apply formatting using [formatting examples](./references/formatting.md)

### Editing or Updating
1. Identify what needs to change (content, styling, structure)
2. Reference [formatting examples](./references/formatting.md) for styling guidance
3. Make changes while maintaining consistent document structure
4. Test compilation with `pdflatex` or your LaTeX compiler
5. Reference [troubleshooting guide](./references/troubleshooting.md) if errors occur

### Troubleshooting Errors
1. Read the error message to identify the problem type
2. Check [troubleshooting guide](./references/troubleshooting.md) for solutions
3. Verify package dependencies in [packages reference](./references/packages.md)
4. Test the fix by recompiling

## Best Practices

- Use consistent formatting throughout documents
- Leverage templates for professional appearance
- Include comments in LaTeX code for clarity
- Test regularly during development
- Keep packages minimal to reduce dependencies
- Use version control for document changes

## Common Packages for Resumes
- `geometry` - Page margins and layout
- `fontawesome5` - Icons for resume
- `xcolor` - Text colors
- `hyperref` - Clickable links
- `fancyhdr` - Headers and footers
- `array` - Table formatting

## Document Structure Template

```
\documentclass{article}
\usepackage{geometry}
\geometry{margin=0.5in}

\usepackage{hyperref}
\hypersetup{colorlinks=true, urlcolor=blue}

\begin{document}

\section{Section Name}
Content here...

\end{document}
```

## Quick Links

- [Package Reference](./references/packages.md) - Common LaTeX packages
- [Formatting Guide](./references/formatting.md) - Styling and layout examples
- [Resume Templates](./assets/templates.tex) - Ready-to-use resume templates
- [Troubleshooting](./references/troubleshooting.md) - Common errors and fixes
- [Style Guide](./references/style-guide.md) - Professional document best practices
