# LaTeX Formatting Examples

Common formatting techniques and code snippets for professional documents and resumes.

## Text Styling

### Basic Formatting

```latex
\textbf{Bold text}
\textit{Italic text}
\underline{Underlined text}
\texttt{Monospace/typewriter}
\textsc{Small caps}
{\color{red}Colored text}
```

### Font Sizes

```latex
\tiny       % Very small
\small      % Small
\normalsize % Normal (default)
\large      % Large
\Large      % Larger
\LARGE      % Even larger
\huge       % Huge
\Huge       % Very huge
```

## Section Formatting

### Headers & Sections

```latex
% Standard sections
\section{Main Section}
\subsection{Subsection}
\subsubsection{Sub-subsection}

% Unnumbered sections
\section*{Section without number}

% Custom section styling (requires titlesec)
\usepackage{titlesec}
\titleformat{\section}
  {\Large\bfseries}
  {}
  {0em}
  {\color{darkblue}}
  [\titlerule]
```

### Section Spacing

```latex
% Reduce space before/after sections
\usepackage{titlesec}
\titlespacing*{\section}{0pt}{6pt}{6pt}
\titlespacing*{\subsection}{0pt}{4pt}{4pt}
```

## Resume-Specific Formatting

### Job Entry Format

```latex
% Job title and dates
\textbf{Software Engineer} \hfill \textit{Jan 2021 -- Present}
\newline
\textit{Tech Company Inc.} \\

% Bullet points
\begin{itemize}[leftmargin=*]
  \item Developed REST APIs using Python and FastAPI
  \item Reduced load time by 40% through optimization
  \item Led team of 3 junior developers
\end{itemize}
```

### Skill Listing

```latex
% Skills in columns
\noindent
\textbf{Languages:} Python, JavaScript, C++, Java \\
\textbf{Frameworks:} React, Django, FastAPI \\
\textbf{Tools:} Git, Docker, Kubernetes, AWS \\

% Skills with categories
\begin{itemize}[leftmargin=*]
  \item \textbf{Frontend:} React, Vue.js, HTML/CSS
  \item \textbf{Backend:} Python, Node.js, PostgreSQL
  \item \textbf{Cloud:} AWS, Docker, Kubernetes
\end{itemize}
```

## Spacing & Layout

### Horizontal Spacing

```latex
\hspace{1cm}        % Fixed horizontal space
\hfill              % Fill to end of line
\quad               % Space equal to font size
\qquad              % Double quad
```

### Vertical Spacing

```latex
\vspace{0.5cm}      % Fixed vertical space
\\[0.2cm]           % Line break with space
\medskip            % Medium vertical space
\smallskip          % Small vertical space
\bigskip            % Big vertical space
```

### Paragraph Spacing

```latex
\setlength{\parskip}{0.5em}    % Space between paragraphs
\setlength{\parindent}{0pt}    % Remove paragraph indentation
```

## Tables

### Simple Table

```latex
\begin{tabular}{l|c|r}
  \textbf{Left} & \textbf{Center} & \textbf{Right} \\
  \hline
  Data 1 & Data 2 & Data 3 \\
  Data 4 & Data 5 & Data 6 \\
\end{tabular}
```

### Professional Table (with booktabs)

```latex
\usepackage{booktabs}
\begin{tabular}{l|l|r}
  \toprule
  \textbf{Skill} & \textbf{Level} & \textbf{Years} \\
  \midrule
  Python & Expert & 5 \\
  React & Proficient & 3 \\
  \bottomrule
\end{tabular}
```

## Colors

### Define Custom Colors

```latex
\usepackage{xcolor}

% Define colors
\definecolor{darkblue}{RGB}{0, 51, 102}
\definecolor{accent}{HTML}{0066CC}

% Use colors
{\color{darkblue}Colored text}
\textcolor{accent}{Another color}
```

### Professional Color Schemes

```latex
% Blue & Gray
\definecolor{primary}{RGB}{0, 51, 102}
\definecolor{secondary}{RGB}{102, 102, 102}

% Green & Teal
\definecolor{primary}{RGB}{0, 102, 102}
\definecolor{secondary}{RGB}{51, 153, 102}

% Purple & Gray
\definecolor{primary}{RGB}{102, 51, 153}
\definecolor{secondary}{RGB}{128, 128, 128}
```

## Icons & Symbols (fontawesome5)

```latex
\usepackage{fontawesome5}

% Contact icons
\faEnvelope   % Email
\faPhone      % Phone
\faLinkedin   % LinkedIn
\faGithub     % GitHub
\faLink       % Website/link
\faMapMarker  % Location

% Example usage
\faEnvelope\ user@example.com \\
\faPhone\ (555) 123-4567 \\
\faLinkedin\ linkedin.com/in/username
```

## Lists

### Bullet Points with Customization

```latex
\usepackage{enumitem}

% Remove left margin
\begin{itemize}[leftmargin=*]
  \item First item
  \item Second item
\end{itemize}

% Custom bullets
\begin{itemize}[label=$\bullet$]
  \item Bullet with symbol
\end{itemize}

% Numbered lists
\begin{enumerate}[leftmargin=*]
  \item First step
  \item Second step
\end{enumerate}
```

## Line Breaks & Dividers

```latex
% Horizontal line
\hrule

% Horizontal line with spacing
\vspace{0.2cm}
\rule{\textwidth}{0.5pt}
\vspace{0.2cm}

% Simple divider
\medskip\hrule\medskip
```
