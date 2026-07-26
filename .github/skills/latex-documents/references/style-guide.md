# LaTeX Style Guide

Best practices for creating professional documents and resumes in LaTeX.

## Document Structure

### Recommended Order

1. **Documentclass** - Define document type
2. **Packages** - Load required packages
3. **Preamble** - Set up geometry, styles, commands
4. **Document** - Main content

```latex
\documentclass[11pt]{article}

% Packages
\usepackage{geometry}
\usepackage{fontawesome5}
\usepackage{hyperref}

% Configuration
\geometry{margin=0.75in}
\pagestyle{empty}
\hypersetup{colorlinks=true, urlcolor=blue}

\begin{document}
% Content here
\end{document}
```

---

## Typography Standards

### Font Sizes for Resumes

| Element | Size | Style |
|---------|------|-------|
| Name/Header | 16-18pt | Bold |
| Section titles | 12-13pt | Bold |
| Job titles | 11pt | Bold |
| Company/dates | 11pt | Regular |
| Body text | 10-11pt | Regular |
| Bullet points | 10-11pt | Regular |

### Font Families

**Professional fonts for LaTeX**:
- **Serif**: Computer Modern (default), Times New Roman
- **Sans-serif**: Helvetica, Arial, Calibri
- **Monospace**: Courier, Courier New

**Recommendation**: Stick with default Computer Modern or use `fontspec` with system fonts:

```latex
% For XeLaTeX/LuaLaTeX
\usepackage{fontspec}
\setmainfont{Calibri}
\setsansfont{Arial}
```

---

## Spacing Guidelines

### Margins

**Standard professional resume margins**:
- Top: 0.5-0.75 inches
- Bottom: 0.5-0.75 inches
- Left: 0.75 inches
- Right: 0.75 inches

```latex
\geometry{top=0.5in, bottom=0.5in, left=0.75in, right=0.75in}
```

### Line Spacing

- **Resume body**: Single spacing (1.0)
- **Between sections**: 0.2-0.3cm
- **Between bullet points**: Automatic or small space

```latex
\setlength{\parskip}{0}    % No space between paragraphs
\setlength{\parindent}{0}  % No indentation
```

### Section Spacing

```latex
\titlespacing*{\section}{0pt}{6pt}{4pt}
\titlespacing*{\subsection}{0pt}{4pt}{2pt}
```

---

## Color Usage

### Professional Color Palettes

**Palette 1: Blue & Gray**
```latex
\definecolor{primary}{RGB}{0, 51, 102}      % Dark blue
\definecolor{secondary}{RGB}{102, 102, 102} % Gray
\definecolor{accent}{RGB}{0, 102, 204}      % Light blue
```

**Palette 2: Green & Teal**
```latex
\definecolor{primary}{RGB}{0, 102, 102}    % Teal
\definecolor{secondary}{RGB}{51, 153, 102}  % Green
\definecolor{accent}{RGB}{0, 153, 153}      % Light teal
```

**Palette 3: Purple & Gray**
```latex
\definecolor{primary}{RGB}{102, 51, 153}   % Purple
\definecolor{secondary}{RGB}{128, 128, 128} % Gray
\definecolor{accent}{RGB}{153, 102, 204}    % Light purple
```

### Color Usage Rules

- **Primary color**: Section headings, name
- **Secondary color**: Dates, company names, dividers
- **Accent color**: Links, highlights
- **Body text**: Black (RGB 0, 0, 0)
- **Limit colors**: Use 2-3 colors maximum

---

## Content Organization

### Effective Section Ordering

1. **Name & Contact** - Top of resume
2. **Professional Summary** (optional) - 2-3 lines
3. **Experience** - Most detailed, reverse chronological
4. **Education** - Institution, degree, graduation date
5. **Skills** - Organized by category
6. **Additional Sections** - Projects, certifications, etc. (if space allows)

### Name & Contact Section

```latex
\noindent
{\Large\textbf{John Doe}}\\
\faEnvelope\ john.doe@email.com \quad
\faPhone\ (555) 123-4567 \quad
\faLinkedin\ linkedin.com/in/johndoe \quad
\faGithub\ github.com/johndoe
```

### Experience Section

```latex
\section*{Experience}

\noindent
\textbf{Senior Software Engineer} \hfill \textit{Jan 2021 -- Present}
\newline
{\color{secondary}Tech Company Inc.} \newline
\begin{itemize}[leftmargin=*,itemsep=0pt]
  \item Led development of microservices architecture serving 1M+ users
  \item Reduced API response time by 60% through optimization
  \item Mentored team of 4 junior developers
\end{itemize}

\vspace{0.1cm}

\noindent
\textbf{Software Engineer} \hfill \textit{Jun 2018 -- Dec 2020}
\newline
{\color{secondary}Another Company Ltd.}
% ... more experience
```

### Skills Section

```latex
\section*{Skills}

\noindent
\textbf{Languages:} Python, JavaScript, Java, C++, SQL \\
\textbf{Frameworks:} Django, React, FastAPI, Spring Boot \\
\textbf{Tools \& Databases:} Git, Docker, PostgreSQL, MongoDB \\
\textbf{Soft Skills:} Leadership, Communication, Problem Solving
```

---

## Professional Standards

### Formatting Consistency

- ✅ Use consistent date formats: "Jan 2021 -- Present"
- ✅ Consistent capitalization: "Software Engineer" (title case)
- ✅ Consistent punctuation in bullet points
- ✅ Use either all bullet points or all paragraphs (not mixed)
- ✅ Align text consistently (left-aligned for resumes)

### ATS (Applicant Tracking System) Compatibility

- Use standard fonts (avoid decorative fonts)
- Avoid graphics, charts, or images (unless PDF is final)
- Use simple formatting (bold, italics OK; avoid colors for text)
- Use standard section headings
- Avoid tables and complex layouts
- Use simple bullet points (• or -)

### Length Guidelines

- **Resume**: 1 page (entry-level to mid-career), 2 pages (senior)
- **Section headings**: Short and clear
- **Bullet points**: 1-2 lines each, 3-5 bullets per job
- **Total bullets per job**: Don't exceed 6 bullets

---

## Common Mistakes to Avoid

1. **Too many fonts** - Stick to 2-3 fonts maximum
2. **Inconsistent spacing** - Use defined spacing values
3. **Too much color** - Limit to 2-3 professional colors
4. **Tiny margins** - Stay within standard margins
5. **Excessive italics** - Use sparingly
6. **Orphaned lines** - Adjust spacing to avoid single lines on next page
7. **Inconsistent formatting** - Bullet points, dates, names should look identical
8. **Dense text** - Use whitespace effectively

---

## Quick Checklist

- [ ] Name and contact info clearly visible at top
- [ ] Consistent date formatting (Month Year -- Month Year)
- [ ] All job titles in bold
- [ ] Bullet points start with action verbs (Led, Developed, Increased)
- [ ] Numbers/metrics included where relevant
- [ ] No more than 2-3 bullets per job (unless senior level)
- [ ] Margins are 0.5-0.75 inches
- [ ] Font size 10-11pt for body text
- [ ] Consistent spacing between sections
- [ ] No spelling or grammar errors
- [ ] Links are clickable in PDF (if using hyperref)
- [ ] Looks professional when printed in black & white
