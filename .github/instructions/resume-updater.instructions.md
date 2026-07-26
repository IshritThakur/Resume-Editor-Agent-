---
description: "How to use the Resume Updater agent: input formats, workflow, examples, and best practices for updating LaTeX and Canva resumes."
applyTo: "**"
---

# Resume Updater Agent - User Instructions

Guide for using the Resume Updater agent to modify and maintain your LaTeX and Canva-based resumes with automatic versioning and backup.

## Quick Start

1. **Open chat** and select the "Resume Updater" agent (or type `/Resume Updater`)
2. **Describe your request** (e.g., "Add a new job at Acme Corp as Senior Engineer")
3. **Provide your resume** (see input formats below)
4. **Agent creates a versioned copy** and applies changes
5. **Review the output** and request modifications if needed

---

## Input Formats

### Option 1: Provide Existing LaTeX File (Recommended)

**Best for**: Already have a `.tex` resume file

**Steps**:
1. Paste the file path to your resume:
   ```
   My resume is at /Users/ishritthakur/my-resume.tex
   
   Please add my new role as Senior Software Engineer at Tech Corp
   ```

2. Agent will:
   - Read your existing LaTeX file
   - Understand the structure and styling
   - Create a versioned copy (e.g., `my-resume_updated_v1.tex`)
   - Apply your requested changes

**Example**:
```
@ResumUpdater

My current resume is at: /Users/ishritthakur/Documents/resume.tex

Please:
1. Add new job: "Senior Software Engineer at Stripe, Jan 2024 - Present"
2. Add achievements: "Led team of 5", "Reduced latency by 40%", "Architected microservices"
3. Update skills section to include "Kubernetes" and "AWS"
```

---

### Option 2: Paste LaTeX Content Directly

**Best for**: Quick updates or file too long to reference by path

**Steps**:
1. Copy your resume LaTeX code and paste it in chat
2. Describe your changes
3. Agent processes and returns updated version

**Example**:
```
@ResumUpdater

Here's my current resume LaTeX:

\documentclass{article}
\usepackage{geometry}
...
[full LaTeX content here]
...
\end{document}

Please update the Experience section to add my new role at Acme.
```

---

### Option 3: Describe Changes Without File (Start from Template)

**Best for**: Starting fresh or major restructuring

**Steps**:
1. Describe your information:
   ```
   Create a new LaTeX resume with:
   - Name: John Smith
   - Experience: 5 years as Software Engineer at Company A, 3 years at Company B
   - Education: BS Computer Science from University
   - Skills: Python, React, AWS, Leadership
   ```

2. Agent creates a resume from template
3. You review and request refinements

**Example**:
```
@ResumUpdater

Create a new resume for me with:
- Name: Sarah Johnson
- Title: Product Manager
- 2 years at TechCorp (managed 3 product launches, 40% revenue growth)
- 3 years at StartupXYZ (built first product team)
- Education: MBA Stanford, BS Economics Yale
```

---

### Option 4: Canva-Based Resume Updates

**Best for**: Resumes designed in Canva instead of LaTeX

**Steps**:
1. Describe your Canva resume and desired changes:
   ```
   I have a Canva resume using the "Modern Minimalist" template
   
   Please create an updated version with:
   - New job role added
   - Skills section reorganized
   - Updated contact information
   ```

2. Agent will:
   - Provide guidance on making these changes in Canva
   - Describe design adjustments needed
   - Offer color/font recommendations

**Note**: Canva agent provides design guidance; for actual Canva edits, you make changes directly in Canva (agent can't edit Canva docs directly)

---

## What the Agent Does

### Creates Versioned Copies
- Original file: `resume.tex` (preserved)
- Updated files: `resume_updated_v1.tex`, `resume_updated_v2.tex`, etc.
- You always have backups

### Maintains Formatting Consistency
- Analyzes your current resume's style
- Matches fonts, colors, spacing in updates
- Keeps visual design consistent

### Handles Common Tasks
- ✓ Add/remove experience entries
- ✓ Modify skills sections
- ✓ Update education information
- ✓ Add projects or certifications
- ✓ Adjust styling and formatting
- ✓ Change colors or fonts
- ✓ Reorganize sections
- ✓ Fix formatting issues

### Provides Preview
Shows you what changed before saving

---

## Request Examples

### Example 1: Add New Work Experience

```
@ResumUpdater

Resume file: /Users/name/resume.tex

Add new job to Experience section:

Position: Senior Software Engineer
Company: Stripe
Dates: Jan 2024 - Present
Location: San Francisco, CA
Achievements:
- Led development of payment processing system for 500+ merchants
- Increased transaction throughput by 60% through optimization
- Mentored team of 4 junior engineers
```

---

### Example 2: Update Skills

```
@ResumUpdater

Resume: /Users/name/Documents/my-resume.tex

Please update the Skills section:

Add these new skills:
- Kubernetes
- TensorFlow
- Rust

Remove:
- Outdated Java Spring

Reorganize order - put Cloud/DevOps first
```

---

### Example 3: Modify Education

```
@ResumUpdater

Resume: /Users/name/resume.tex

Update Education section:

Add: AWS Certified Solutions Architect - Associate (May 2024)
Add: Google Cloud Professional Cloud Architect (Aug 2023)

Remove: Old certification (if expired or not relevant)
```

---

### Example 4: Comprehensive Refresh

```
@ResumUpdater

Resume: /Users/name/resume.tex

This is a comprehensive update - please:

1. Add new job (most recent):
   - Software Engineer at TechCorp, Jun 2023 - Present
   - [3-4 key achievements with metrics]

2. Update skills to emphasize:
   - Python, React, AWS, Docker
   - Remove outdated Flash and jQuery

3. Add new certification:
   - AWS Solutions Architect (May 2024)

4. Refine language on all achievements:
   - Use stronger action verbs
   - Add quantifiable metrics where possible
   - Keep bullets to 1-2 lines each

5. Check formatting:
   - Ensure dates are consistent (Month Year format)
   - Verify all sections align properly
   - Make sure it fits on one page
```

---

## Input Checklist

Before submitting your request, ensure:

- [ ] **Clear description** - What changes do you want? Be specific.
- [ ] **File path or content provided** - LaTeX file path or pasted content
- [ ] **Specific details** - Dates, company names, achievements with numbers
- [ ] **Format consistency** - If you have existing resume, maintain its style
- [ ] **One major change at a time** (optional) - Multiple small changes ok, but one big restructuring per request works better

---

## Output Format

The agent provides:

1. **New file path**: Where the versioned copy was saved
   ```
   Created: /Users/ishritthakur/resume_updated_v2.tex
   ```

2. **Summary of changes**: What was modified
   ```
   - Added: New job at Tech Corp (Jan 2024 - Present)
   - Updated: Skills section with Kubernetes and AWS
   - Modified: Formatting to maintain consistency
   ```

3. **Preview snippet**: Key sections that changed
   ```
   \textbf{Senior Software Engineer} \hfill \textit{Jan 2024 -- Present}
   \newline
   {\color{secondary}Tech Corp Inc., San Francisco, CA}
   ```

4. **Next steps**: Suggestion for further changes
   ```
   Would you like me to:
   - Adjust formatting/spacing?
   - Add more achievements?
   - Change colors or styling?
   - Create variations for different roles?
   ```

---

## Best Practices

### DO
- ✓ Be specific about what you want to change
- ✓ Include metrics and numbers (40% improvement, 5+ years, etc.)
- ✓ Use strong action verbs (Led, Developed, Increased, etc.)
- ✓ Keep achievements 1-2 lines per bullet
- ✓ Request one or two changes at a time initially
- ✓ Review the agent's work before confirming
- ✓ Save versioned files (agent does this automatically)
- ✓ Use for both content and styling updates

### DON'T
- ✗ Don't provide vague descriptions ("Make it better")
- ✗ Don't mix formatting styles in your input
- ✗ Don't delete the original resume file
- ✗ Don't share resumes with sensitive personal info
- ✗ Don't request changes that aren't resume-related
- ✗ Don't try to modify Canva resume directly (give guidance instead)

---

## Common Requests

### "I got a new job, add it"
```
@ResumUpdater
Resume: /path/to/resume.tex

New job added to top of Experience:
- Title: [Job Title]
- Company: [Company Name]  
- Dates: [Month Year - Present/End Date]
- Location: [City, State]
- Key achievements: [3-4 items with metrics]
```

### "Update my skills"
```
@ResumUpdater
Resume: /path/to/resume.tex

Skills to ADD: [List new skills]
Skills to REMOVE: [List outdated ones]
Skills to EMPHASIZE: [List of top skills]
```

### "Make it more impactful"
```
@ResumUpdater
Resume: /path/to/resume.tex

Please improve the language in Experience section:
- Use stronger action verbs
- Add metrics/numbers to show impact
- Ensure 1-2 lines per bullet max
```

### "Create role-specific version"
```
@ResumUpdater
Resume: /path/to/resume.tex

Create a version optimized for: [Tech/Finance/Creative/etc]
- Emphasize relevant skills for this role
- Reorganize achievements to highlight most relevant
- Save as: resume_[roletype].tex
```

---

## Versioning & File Management

### Automatic Versioning
- Each update creates a new numbered version
- Original always preserved
- Pattern: `resume_updated_v1.tex`, `resume_updated_v2.tex`, etc.

### Recommended File Organization
```
📁 Resume/
  ├── resume.tex (original/master)
  ├── resume_updated_v1.tex (first update)
  ├── resume_updated_v2.tex (second update)
  ├── resume_tech.tex (tech-specific version)
  └── resume_design.tex (design-specific version)
```

### Managing Versions
- Keep numbered versions for history
- Once satisfied with update, you can rename:
  - `resume_updated_v5.tex` → `resume.tex` (make it new master)
- Delete old versions after confirming update is good
- Archive old versions if needed for reference

---

## Troubleshooting

### "Agent says it can't find my file"
- Check the file path is correct
- Verify file exists and is readable
- Try pasting content directly instead

### "Formatting looks different after update"
- Review [LaTeX Style Guide](../skills/latex-documents/references/style-guide.md)
- Request agent to "maintain original formatting more strictly"
- Check font sizes, spacing, and colors match

### "Changes didn't apply correctly"
- Provide more specific details about desired changes
- Give an example of exactly what you want
- Request agent to create a preview before final version

### "Want to revert to previous version"
- All old versions saved (v1, v2, etc.)
- Use previous version file directly
- Or request agent to restore from archive

---

## Tips for Best Results

1. **Be descriptive**: "Add a job at Acme Corp with responsibilities X, Y, Z"
   (Better than: "Update resume")

2. **Include context**: Your role, industry, target job can help agent prioritize

3. **Use examples**: If you want specific formatting, show an example

4. **One thing at a time**: Multiple small requests > one huge request

5. **Review output**: Check the agent's work before using the new version

6. **Keep originals**: Don't delete old versions until you're completely satisfied

---

## Related Resources

For LaTeX and design help, use these skills:

- **`/latex`** - LaTeX Documents skill for creating/troubleshooting LaTeX
- **`/canva`** - Canva Design skill for design improvements and best practices
- **LaTeX Templates** - [Ready-to-use resume template](../skills/latex-documents/assets/templates.tex)
- **Design Checklist** - [Quality criteria](../skills/canva-design/references/design-checklist.md)
- **Color & Fonts** - [Professional recommendations](../skills/canva-design/references/colors-fonts.md)

---

## Support & Feedback

### If something doesn't work:
1. Check this guide for common issues
2. Review the LaTeX skill for syntax help
3. Consult design resources for styling questions
4. Provide more detailed input to agent

### To improve the agent:
- Describe what would work better
- Suggest new capabilities
- Share examples of what you need
