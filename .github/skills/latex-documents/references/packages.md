# LaTeX Packages Reference

Common packages used in LaTeX documents, especially for resumes and professional documents.

## Page Layout & Geometry

| Package | Purpose | Example |
|---------|---------|---------|
| `geometry` | Control page margins, paper size | `\geometry{margin=0.75in}` |
| `fancyhdr` | Customize headers and footers | `\pagestyle{fancy}` |
| `multicol` | Multiple columns in document | `\begin{multicols}{2}` |

## Fonts & Text Formatting

| Package | Purpose | Example |
|---------|---------|---------|
| `fontawesome5` | Icons for contacts (email, phone, LinkedIn) | `\faEnvelope, \faPhone` |
| `xcolor` | Text colors and highlighting | `{\color{blue}Colored text}` |
| `soul` | Text effects (strikethrough, highlighting) | `\hl{highlighted}` |
| `fontspec` | Use system fonts (XeLaTeX/LuaLaTeX) | `\setmainfont{Arial}` |

## Tables & Arrays

| Package | Purpose | Example |
|---------|---------|---------|
| `array` | Enhanced table formatting | `\begin{tabular}{l\|r}` |
| `booktabs` | Professional table layouts | `\toprule, \midrule, \bottomrule` |
| `tabu` | Flexible table environment | `\begin{tabu}` |

## Links & References

| Package | Purpose | Example |
|---------|---------|---------|
| `hyperref` | Clickable links and bookmarks | `\href{url}{text}` |
| `url` | Proper URL formatting | `\url{https://example.com}` |

## Lists & Formatting

| Package | Purpose | Example |
|---------|---------|---------|
| `enumitem` | Customize list formatting | `\begin{itemize}[leftmargin=*]` |
| `ragged2e` | Text alignment options | `\RaggedRight` |

## Minimal Resume Setup

```latex
\documentclass[11pt]{article}

% Packages
\usepackage{geometry}
\usepackage{fontawesome5}
\usepackage{hyperref}
\usepackage{xcolor}
\usepackage{enumitem}

% Geometry
\geometry{margin=0.75in}

% Remove header/footer
\pagestyle{empty}

% Hyperlink colors
\hypersetup{colorlinks=true, urlcolor=blue}

\begin{document}

% Document content here

\end{document}
```

## Best Practices

- Load packages in logical order (geometry, fonts, colors, formatting)
- Use specific packages rather than loading everything
- Comment packages for clarity on why each is included
- Test document after adding new packages for conflicts
