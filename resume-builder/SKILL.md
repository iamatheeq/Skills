---
name: resume-builder
description: Build or improve professional, truthful, ATS-oriented resumes from minimal user-provided career information. Ask only for missing mandatory facts, intelligently enhance wording and structure, validate content and consistency, and produce a polished final resume without fabricating facts.
---

# Resume Builder

## Mission

Transform minimal, factual career information into a professional, targeted, readable, ATS-oriented resume.

Core workflow:

**Minimal Input → Intelligent Enhancement → Validation → Professional Resume**

The skill improves presentation and wording, but must never invent employment history, achievements, metrics, technologies, qualifications, certifications, employers, dates, or other facts.

## When to Use

Use this skill when the user wants to:
- Create a resume/CV from raw information.
- Improve or rewrite an existing resume.
- Tailor a resume to a target role or job description.
- Make a resume more professional and ATS-friendly.
- Convert rough experience notes into strong resume content.

Do not require the user to already know resume-writing terminology.

## Project Adoption

At the start of a new resume project:
1. Determine whether the user is creating a new resume or improving an existing one.
2. Reuse information already supplied in the current task or attached resume.
3. Ask only for missing mandatory information.
4. If a job description is supplied, analyze it before final writing.
5. Keep the user's factual career history as the source of truth.
6. Preserve a master profile when the environment supports persistent project data, so multiple targeted versions can be generated without re-entering facts.

## Minimal Input

Request these mandatory fields when they are unavailable:

1. Full name
2. Target job title/role
3. Email
4. Phone
5. Location
6. Professional experience
7. Education
8. Skills

Experience input may be rough notes. For each role, collect whatever the user knows about:
- Employer
- Job title
- Start/end dates or present status
- Responsibilities/work performed
- Technologies/tools
- Projects
- Outcomes/achievements, if known

If the user does not know an optional detail, do not block generation.

### Optional Information

Collect only when relevant or available:
- LinkedIn
- GitHub
- Portfolio
- Professional headline
- Existing professional summary
- Projects
- Certifications
- Awards
- Publications
- Languages
- Volunteer experience
- Professional memberships
- Target company
- Target industry
- Job description

Do not force optional sections into the resume.

## Adaptive Questioning

Do not ask a giant questionnaire when information can be gathered progressively.

Preferred interaction:
1. Ask for the minimum missing fields.
2. Identify gaps in experience/education/skills.
3. Ask focused follow-up questions only where the missing information materially affects quality.
4. Allow the user to say “skip” for optional fields.

If the user supplies an existing resume, extract and validate its information instead of asking them to repeat it.

## Input UI Contract

When the host environment supports structured input controls, present fields as appropriate input boxes/forms rather than requiring one large free-text prompt.

Recommended controls:
- Single-line inputs: name, job title, email, phone, location, links.
- Date inputs: employment and education dates.
- Multiline inputs: summary notes, responsibilities, achievements, project descriptions.
- Repeatable groups: work experience, education, projects, certifications, awards.
- Tag/chip input: skills and technologies.
- File upload: existing resume and job description when supported.

The skill defines the data and validation contract; the host UI decides the exact visual control implementation.

## Intelligent Enhancement

Rewrite raw information into concise, professional resume language.

### Professional Writing
- Use strong, accurate action verbs.
- Prefer specific responsibilities and outcomes over generic statements.
- Remove repetition and filler.
- Improve grammar, spelling, clarity, and concision.
- Use terminology appropriate to the target role.
- Preserve technical accuracy.
- Keep tense consistent: current roles generally use present tense; previous roles generally use past tense.
- Prioritize impact, ownership, scope, and relevant technologies.

### Quantification
Use numbers only when the user provides them or explicitly confirms them.

Allowed:
- “Reduced response time by 30%” when the user supplied 30%.
- “Supported a team of 8 developers” when the user supplied 8.

Not allowed:
- Inventing percentages, revenue, user counts, team sizes, performance gains, or business results.

If an achievement is qualitative, write it strongly without fabricating a metric.

### Professional Headline
Generate a concise headline when useful from verified facts, for example:
`Senior Full Stack Developer | React | .NET | SQL Server`

Do not add technologies merely because they are common for the role.

### Professional Summary
Generate a short, role-targeted summary from verified experience, skills, domain knowledge, and achievements. Avoid generic claims such as “hardworking” unless the user explicitly wants them and they are supported by context.

### Experience Bullets
Convert rough notes into achievement-oriented bullets where the source information supports them.

Prefer:
`Action + what was built/done + technology/domain + verified outcome`

Do not turn ordinary responsibility into an invented achievement.

### Skills
Organize verified skills into relevant categories such as:
- Programming Languages
- Frontend
- Backend
- Databases
- Cloud/DevOps
- Tools
- Frameworks
- Other relevant technical skills

Do not add skills solely because they appear in the job description.

## Job Description Optimization

When a job description is provided:
1. Extract target role, required skills, preferred skills, responsibilities, domain terms, and meaningful keywords.
2. Compare those requirements with verified candidate information.
3. Identify strong matches and gaps.
4. Emphasize genuine matching experience and skills.
5. Use job-description terminology where truthful and natural.
6. Never add a missing skill or experience merely to improve keyword matching.
7. Avoid keyword stuffing.

If no job description exists, optimize for the stated target job title and industry without pretending to know a specific employer's ATS rules.

## Resume Structure

Default professional structure:
1. Name and contact information
2. Professional headline
3. Professional summary
4. Skills
5. Professional experience
6. Projects, when relevant
7. Education
8. Certifications, awards, publications, languages, or other optional sections when useful

Reorder sections when the candidate's seniority or target role makes another hierarchy more effective.

## ATS Quality Rules

Aim for broad ATS compatibility:
- Use conventional section names.
- Keep important content as selectable text.
- Use simple, predictable document structure.
- Avoid decorative layouts that can interfere with parsing.
- Avoid placing essential information only in headers, footers, images, icons, or graphics.
- Keep dates and job titles explicit.
- Use consistent formatting.
- Use standard bullets.
- Match relevant terminology naturally.
- Keep contact information machine-readable.

Never claim guaranteed compatibility with every ATS. ATS products and employer configurations vary.

## Validation Pipeline

Before presenting the final resume, run these checks:

### 1. Required Information
- Name present
- Target role present
- Contact information present
- Experience present when applicable
- Education present
- Skills present

### 2. Accuracy / No Fabrication
- Every factual claim traces to user-provided information.
- No invented metrics.
- No invented employers, projects, tools, qualifications, awards, or dates.
- No unsupported seniority claims.

### 3. Consistency
- Dates do not conflict without explanation.
- Job titles and employers are consistent.
- Technology names are consistent.
- Current/past tense is appropriate.
- Education details are consistent.

### 4. Writing Quality
- Grammar and spelling checked.
- Bullets are concise.
- Repetition removed.
- Strong verbs used appropriately.
- Summary is targeted.

### 5. ATS Structure
- Standard sections.
- Parser-friendly ordering.
- No critical information trapped in graphics.
- Keywords are relevant and natural.

### 6. Relevance
- Most relevant experience appears prominently.
- Skills align with the target role when supported by evidence.
- Irrelevant content is reduced rather than artificially expanded.

### 7. Readability
- Clear hierarchy.
- Consistent spacing.
- Scannable bullets.
- Appropriate length for seniority and career history.

## Quality Gate

Internally classify each category as PASS, NEEDS REVIEW, or FAIL.

Recommended final report:
- Required information: PASS/NEEDS REVIEW
- Accuracy/no fabrication: PASS/NEEDS REVIEW/FAIL
- Professional writing: PASS/NEEDS REVIEW
- ATS structure: PASS/NEEDS REVIEW
- Keyword alignment: PASS/NEEDS REVIEW
- Consistency: PASS/NEEDS REVIEW
- Readability: PASS/NEEDS REVIEW

Do not present a perfect score if a meaningful issue remains.

## Output Modes

Support:

### New Resume
Produce the polished resume after validation.

### Resume Improvement
Show the improved resume and, when useful, a concise list of major improvements.

### Job-Specific Resume
Produce a targeted version based on the supplied job description and verified profile.

### Review Only
If the user asks for analysis rather than rewriting, provide findings without silently changing the resume.

## Do

- Ask only for missing mandatory facts.
- Let users provide rough notes.
- Improve wording substantially while preserving facts.
- Tailor content to the target role when evidence supports it.
- Validate dates, terminology, grammar, structure, and relevance.
- Use standard ATS-friendly structure.
- Clearly identify anything that needs user confirmation.
- Preserve optional sections only when they add value.

## Don't

- Do not invent achievements or metrics.
- Do not add skills because they are fashionable or requested by a job description if the user does not have them.
- Do not claim the resume is guaranteed to pass every ATS.
- Do not force users to fill optional fields.
- Do not produce a generic keyword-stuffed resume.
- Do not hide important information in graphics or decorative elements.
- Do not substantially change factual dates, titles, employers, qualifications, or career history.

## Final Delivery Standard

A successful output should be:
- Professional
- Truthful
- Targeted
- Concise
- ATS-oriented
- Easy to scan
- Consistent
- Ready for the user to review and submit

The final resume is a polished representation of the user's supplied facts, not a fictional reconstruction of their career.
