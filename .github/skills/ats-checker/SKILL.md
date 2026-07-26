---
description: "Analyze resumes for Applicant Tracking System (ATS) compatibility, score them, and suggest enhancements to improve parsing and keyword matching."
applyTo: "**"
---

# ATS Checker Skill

Analyze your resume's compatibility with Applicant Tracking Systems (ATS) used by most employers. This skill evaluates formatting, keyword optimization, and readability to ensure your resume gets past automated screening.

## What It Does

- **ATS Compatibility Analysis**: Checks resume format, fonts, and structure for ATS-friendliness
- **Keyword Optimization**: Analyzes keyword density and suggests additions based on job descriptions
- **Readability Scoring**: Evaluates text clarity and structure
- **Enhancement Suggestions**: Provides specific recommendations to improve ATS performance
- **Scoring System**: Rates resume on a 0-100 scale with detailed breakdown

## When to Use

- Before applying to jobs through online portals
- When your resume isn't getting interview callbacks
- To optimize for specific job postings
- After major resume updates

## How to Use

### Basic Analysis
```
@ATSChecker analyze my resume at /path/to/resume.pdf
```

### Job-Specific Optimization
```
@ATSChecker optimize for software engineer role using this job description: [paste JD]
Resume: /path/to/resume.pdf
```

### Full Enhancement
```
@ATSChecker enhance resume at /path/to/resume.tex for AI engineer positions
```

## Workflow

1. **Input Validation**: Accepts PDF, LaTeX (.tex), or plain text resumes
2. **Text Extraction**: Parses resume content (PDF text extraction for PDFs)
3. **ATS Analysis**:
   - Format check (standard fonts, no graphics, proper headings)
   - Keyword analysis (frequency, relevance)
   - Structure validation (sections, contact info)
   - Readability metrics
4. **Scoring**: Calculates overall ATS score with category breakdowns
5. **Recommendations**: Suggests specific improvements
6. **Optional Enhancement**: Generates improved version if requested

## Output Format

### Analysis Report
```
ATS Compatibility Score: 78/100

📊 **Breakdown:**
- Formatting: 85/100
- Keywords: 70/100
- Readability: 80/100

🔍 **Issues Found:**
- Low keyword density for "machine learning"
- Complex formatting may confuse parsers
- Missing quantifiable achievements

💡 **Suggestions:**
- Add 3-5 instances of "Python" and "AI"
- Use standard section headers
- Include more metrics in experience bullets
```

### Enhanced Version
When enhancement is requested, provides:
- Updated resume file (e.g., `resume_ats_optimized.pdf`)
- Change summary
- New ATS score

## Best Practices

### Resume Optimization Tips
- Use standard fonts (Arial, Calibri, Times New Roman)
- Include relevant keywords naturally
- Avoid tables, columns, or complex layouts
- Use clear section headers
- Include contact info at top
- Save as PDF for consistency

### Keyword Strategy
- Research job descriptions for common terms
- Include 5-15 relevant keywords
- Balance keyword density (1-2% recommended)
- Use variations (e.g., "machine learning", "ML", "artificial intelligence")

## Examples

### Example 1: Basic Check
```
@ATSChecker
Check my resume: /Users/john/resume.pdf
```

### Example 2: Job-Targeted
```
@ATSChecker optimize for data scientist
Job requirements: Python, machine learning, SQL, statistics
Resume file: resume.pdf
```

### Example 3: Full Enhancement
```
@ATSChecker
Enhance this LaTeX resume for software engineering jobs:
File: /path/to/resume.tex
Focus on: Java, Spring Boot, microservices, AWS
```

## Limitations

- Cannot modify graphics or complex PDF elements
- Keyword suggestions based on general ATS patterns
- Enhancement works best with LaTeX source files
- Score is approximate - actual ATS performance varies

## Related Skills

- **latex-documents**: For LaTeX resume editing
- **canva-design**: For visual resume design
- **resume-updater**: For content updates

## Troubleshooting

**Low Score Issues:**
- Complex formatting: Simplify layout, remove graphics
- Missing keywords: Research job postings, add relevant terms
- Poor readability: Use shorter sentences, clear structure

**Enhancement Not Working:**
- Ensure LaTeX file is valid and compilable
- Check file permissions
- For PDFs, ensure text is selectable (not image-based)

## Customization

This skill can be extended to:
- Industry-specific keyword databases
- Custom scoring algorithms
- Integration with job board APIs
- Automated job matching