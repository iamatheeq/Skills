# Resume Builder Skill

## Purpose

`resume-builder` is a standalone selectable skill for turning minimal career information into a professional, truthful, ATS-oriented resume.

Its design principle is:

**Minimal Input → Intelligent Enhancement → Validation → Professional Resume**

The user does not need to know how to write a resume. They can provide rough notes, and the skill improves wording, structure, relevance, and presentation.

## Use Case

Select this skill when you want to:

- Create a new resume from basic information.
- Rewrite an existing resume.
- Turn rough work-experience notes into professional bullets.
- Tailor a resume to a target job.
- Improve ATS-oriented structure and keyword alignment.
- Validate resume quality before submission.

## How to Use

Typical request:

> Create my professional resume using the Resume Builder skill.

The skill should then:

1. Determine whether you are creating or improving a resume.
2. Reuse information already available.
3. Ask only for missing mandatory information.
4. Use structured input controls when the host environment supports them.
5. Accept rough, unpolished descriptions.
6. Enhance the language and resume structure.
7. Analyze a job description if one is supplied.
8. Validate the result for accuracy, consistency, readability, and ATS-oriented structure.
9. Return the final professional resume.

## Minimum Information

Provide:

- Full name
- Target job title
- Email
- Phone
- Location
- Professional experience
- Education
- Skills

You do **not** need to manually write:

- Professional headline
- Professional summary
- Polished experience bullets
- Skill categories
- Achievement wording

The skill can generate these from your factual information.

## Optional Information

You can also provide:

- LinkedIn
- GitHub
- Portfolio
- Projects
- Certifications
- Awards
- Publications
- Languages
- Target company
- Target industry
- Job description

Optional fields can be skipped.

## Example Input

```text
Name: John Doe
Target Job: Senior Full Stack Developer
Email: john@example.com
Phone: +91 XXXXX XXXXX
Location: Chennai, India

Experience:
2022-Present, ABC Technologies, Software Developer
I build React screens and .NET APIs. Work with SQL Server.
Fix production issues and work with the backend team.

2019-2022, XYZ Solutions, Junior Developer
Worked on web applications and REST APIs.

Education:
B.E. Computer Science, ABC University, 2019

Skills:
React, JavaScript, .NET Core, SQL Server, Git
```

The skill converts this into professional resume language without inventing metrics or achievements.

## Job-Specific Example

You can provide a job description together with the same profile:

```text
Create a resume for this job description:
[paste job description]
```

The skill identifies relevant requirements and emphasizes matching experience and skills, while refusing to invent missing qualifications.

## Quality Model

The skill validates:

- Required information
- Accuracy and no fabrication
- Professional writing
- ATS-oriented structure
- Keyword alignment
- Date and terminology consistency
- Readability
- Relevance

A quality gate can report `PASS`, `NEEDS REVIEW`, or `FAIL` for each category.

## Important ATS Note

The skill is designed for broad ATS compatibility, but no system can honestly guarantee that a resume will pass every ATS. Different employers use different ATS products, configurations, parsing rules, and screening processes.

## Important Truthfulness Rule

The skill may improve wording, but it must not fabricate:

- Metrics
- Achievements
- Technologies
- Job responsibilities
- Employers
- Dates
- Certifications
- Degrees
- Awards
- Projects
- Job titles

If a stronger statement requires information that is missing, the skill should ask for confirmation or use a truthful non-quantified statement.

## Standalone Skill Selection

This skill is independent from the other skills in the collection.

- Need technology selection? Select `technology-guide`.
- Need a 3D web experience? Select `3d-web-experience`.
- Need typography standards? Select `typography-system`.
- Need themes and color tokens? Select `theme-system`.
- Need a professional resume? Select `resume-builder`.

Multiple skills can be combined when the host environment supports that workflow, but `resume-builder` does not require the other skills.
