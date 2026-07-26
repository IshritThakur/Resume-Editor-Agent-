# LaTeX Troubleshooting Guide

Solutions for common LaTeX errors and issues.

## Compilation Errors

### "Undefined control sequence"

**Problem**: You used a command that LaTeX doesn't recognize.

**Solutions**:
- Check the command spelling (e.g., `\bf` vs `\textbf{}`)
- Ensure the package providing the command is loaded:
  ```latex
  \usepackage{fontawesome5}  % Needed for \faEnvelope
  ```
- Check for typos in custom macros

**Example Fix**:
```latex
% ❌ Wrong
{\color{red}Text}  % without xcolor package

% ✅ Correct
\usepackage{xcolor}
{\color{red}Text}
```

---

### "Missing $ inserted" or "Extra $ removed"

**Problem**: Math mode is not properly opened/closed with `$` symbols.

**Solutions**:
- Check all `$` symbols are paired
- Use `$$` for display math mode
- Escape special characters outside math mode

**Example Fix**:
```latex
% ❌ Wrong
The formula a+b=c should be emphasized

% ✅ Correct
The formula $a+b=c$ should be emphasized
```

---

### "File not found"

**Problem**: LaTeX can't find an included file or image.

**Solutions**:
- Verify file path is correct and relative to `.tex` file
- Check file actually exists
- Use correct path separators
- Try absolute path for debugging

**Example Fix**:
```latex
% ❌ Wrong
\includegraphics{images/photo}  % Missing file extension

% ✅ Correct
\includegraphics{images/photo.png}
```

---

### "Missing \begin{document}" or "Mismatched \end"

**Problem**: Document structure is incomplete or brackets are mismatched.

**Solutions**:
- Ensure document begins with `\begin{document}` and ends with `\end{document}`
- Check all `\begin{}...\end{}` pairs are matched
- Count opening and closing braces `{` and `}`

**Example Fix**:
```latex
% ❌ Wrong
\documentclass{article}
\begin{document}
\section{Title}
Text here
% Missing \end{document}

% ✅ Correct
\documentclass{article}
\begin{document}
\section{Title}
Text here
\end{document}
```

---

### "Paragraph ended before ... was complete"

**Problem**: You ended a paragraph before completing a command or environment.

**Solutions**:
- Don't put blank lines inside commands
- Ensure environments are closed before paragraph break

**Example Fix**:
```latex
% ❌ Wrong
\textbf{Bold text

another paragraph}

% ✅ Correct
\textbf{Bold text}

Another paragraph
```

---

## Layout Issues

### Text overlaps or extends past page margins

**Problem**: Content is bleeding off the page.

**Solutions**:
- Adjust page margins with `geometry` package:
  ```latex
  \usepackage{geometry}
  \geometry{margin=0.75in}
  ```
- Reduce font size or column width
- Use `\raggedright` for ragged right alignment instead of justified

**Example**:
```latex
\usepackage{geometry}
\geometry{left=0.75in, right=0.75in, top=0.5in, bottom=0.5in}
```

---

### Extra blank pages appearing

**Problem**: Document has unexpected blank pages.

**Solutions**:
- Remove extra `\newpage` or `\clearpage` commands
- Check for `\section` that automatically starts new page
- Use `\usepackage{geometry}` and `\pagestyle{empty}` to disable headers/footers

**Example**:
```latex
\pagestyle{empty}  % Remove default headers/footers
```

---

### Text not wrapping or lines too long

**Problem**: Words extend past margin or don't wrap properly.

**Solutions**:
- Set proper text width with `geometry`
- Use `\raggedright` for left-aligned text without hyphenation
- Break long URLs with `\url{}` or `\href{}`

**Example**:
```latex
\usepackage[hyphens]{url}
\urlstyle{same}
\url{https://very-long-url-that-needs-wrapping.com}
```

---

## Font & Color Issues

### Font not rendering correctly

**Problem**: Text appears in wrong font or italics/bold not showing.

**Solutions**:
- Use proper formatting commands: `\textbf{}` not `\bf`
- Ensure font package is loaded
- Check PDF viewer supports the font

**Example**:
```latex
% ❌ Wrong
{\bf Bold text}
{\it Italic text}

% ✅ Correct
\textbf{Bold text}
\textit{Italic text}
```

---

### Colors not showing in PDF

**Problem**: Colors appear in LaTeX editor but not in compiled PDF.

**Solutions**:
- Ensure `xcolor` package is loaded
- Check color model (RGB vs HTML)
- Try recompiling

**Example**:
```latex
\usepackage{xcolor}
% Define color with RGB (0-255)
\definecolor{myred}{RGB}{255, 0, 0}
% Or use HTML colors
\definecolor{myblue}{HTML}{0066CC}
```

---

## Package Conflicts

### Two packages don't work together

**Problem**: Document won't compile after adding a new package.

**Solutions**:
- Load conflicting packages in specific order
- Remove one package and rebuild to identify culprit
- Check package documentation for known conflicts

**Common conflicts**:
- `babel` + `hyperref` (load hyperref last)
- `tikz` + other drawing packages (load tikz first)

**Example**:
```latex
% ✅ Correct order
\usepackage{fontspec}
\usepackage{babel}
\usepackage{hyperref}  % Load last
```

---

## Resume-Specific Issues

### Resume content gets cut off or disappears

**Problem**: Some content doesn't appear in PDF.

**Solutions**:
- Check margins aren't too small
- Reduce font size with `\small` or `\tiny`
- Remove unnecessary spacing
- Use `\raggedright` to save space

**Example**:
```latex
\geometry{margin=0.6in}  % Reduce margins
\small                   % Reduce font size
```

---

### Bullet points don't align properly

**Problem**: Bullet points have inconsistent indentation.

**Solutions**:
- Use `enumitem` with `leftmargin=*`
- Ensure consistent indentation in source code

**Example**:
```latex
\usepackage{enumitem}
\begin{itemize}[leftmargin=*]
  \item First item
  \item Second item
\end{itemize}
```

---

## Debugging Tips

1. **Locate the error** - LaTeX error messages show line numbers; look for errors near that line
2. **Reduce to minimal case** - Comment out sections to find problematic code
3. **Check brackets** - Use editor with bracket matching to find mismatches
4. **Online compiler** - Try Overleaf.com to test if issue is local
5. **Read full error message** - LaTeX errors provide context; don't just fix the first line
6. **Clear cache** - Delete `.aux`, `.log`, `.out` files and recompile
