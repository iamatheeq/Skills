# 🤖 AI Skills Repository

Welcome to the **Skills Repository** — a modular, reusable, and human-readable library of custom AI skills.

This repository contains independently maintained AI skills that define how an AI assistant should reason, collect information, perform tasks, validate results, and produce consistent outputs.

Each skill is self-contained and can be selected or used independently depending on the task.

---
 
## 🎯 Purpose

The purpose of this repository is to maintain a centralized collection of reusable AI skills.

Instead of creating a new prompt for every project, task, or workflow, each capability is defined as a dedicated skill.

A skill can contain:

- AI behavior and instructions
- Task-specific workflows
- Input requirements
- Validation rules
- Output requirements
- Usage documentation
- Examples
- Best practices
- Do / Don't guidelines
- Project adoption guidance

The goal is to make AI behavior **consistent, reusable, maintainable, and easy to understand**.

---

## 📂 Repository Structure

Every skill is organized inside its own folder.

The standard structure is:

```text
skills/
│
├── typography-skill/
│   ├── skill.md
│   └── README.md
│
├── theme-style/
│   ├── skill.md
│   └── README.md
│
├── technology-guide/
│   ├── skill.md
│   └── README.md
│
├── 3d-web-experience/
│   ├── skill.md
│   └── README.md
│
├── resume-builder/
│   ├── skill.md
│   └── README.md
│
└── README.md
```

Each folder represents **one independent AI capability**.

---

# 🧩 Skill Structure

Every skill should follow the same basic structure:

```text
<skill-name>/
├── skill.md
└── README.md
```

### `skill.md`

The `skill.md` file is the **core AI skill definition**.

It contains the instructions that define how the AI should behave when the skill is selected.

Typical contents include:

```text
Description
Purpose
Activation / Usage
Role / Persona
Workflow
Input Requirements
Decision Rules
Validation
Output Requirements
Do / Don't
Project Adoption
Examples
```

### `README.md`

The `README.md` file explains the skill to humans.

It should describe:

- What the skill does
- When to use it
- What problem it solves
- How to use it
- Expected inputs
- Expected outputs
- Example usage
- Limitations or important notes

The README is documentation for the **developer/user**, while `skill.md` is the instruction set for the **AI**.

---

# 🚀 How to Add a New Skill

Follow these steps when adding a new skill.

### Step 1 — Create the skill folder

Use lowercase letters and hyphens.

```text
my-new-skill/
```

Examples:

```text
resume-builder/
technology-guide/
typography-skill/
theme-style/
code-reviewer/
api-design/
```

---

### Step 2 — Create `skill.md`

Inside the folder, create:

```text
my-new-skill/
└── skill.md
```

The filename should be exactly:

```text
skill.md
```

This file contains the actual AI instructions.

---

### Step 3 — Create `README.md`

Add:

```text
my-new-skill/
├── skill.md
└── README.md
```

The README should explain how developers/users can understand and use the skill.

---

### Step 4 — Define the skill workflow

A good skill should clearly define:

```text
User Request
     ↓
Understand Intent
     ↓
Collect Required Information
     ↓
Process / Execute
     ↓
Validate
     ↓
Generate Result
     ↓
Final Review
```

The workflow should be deterministic wherever practical and should avoid unnecessary questions.

---

### Step 5 — Add the skill to the repository

The final structure should look like:

```text
skills/
└── my-new-skill/
    ├── skill.md
    └── README.md
```

Then commit and push the changes to the repository.

---

# 🧠 Skill Design Principles

All skills in this repository should follow these principles.

## 1. Modular

Each skill should solve a specific problem.

For example:

```text
technology-guide
        ↓
Technology selection
```

while:

```text
3d-web-experience
        ↓
3D web implementation
```

and:

```text
typography-skill
        ↓
Typography system
```

and:

```text
resume-builder
        ↓
Professional resume creation
```

Avoid creating one large skill that tries to solve unrelated problems.

---

## 2. Independent

A skill should work independently whenever possible.

For example, selecting:

```text
resume-builder
```

should not require:

```text
typography-skill
theme-style
technology-guide
```

unless there is an explicit reason to combine them.

Skills may be combined when a project requires multiple capabilities.

---

## 3. Human-Readable

Skill files should be easy for developers to understand and maintain.

Prefer:

```markdown
## Input Requirements

The skill requires:

- Target job title
- Work experience
- Education
- Skills
```

instead of undocumented or opaque instructions.

---

## 4. Action-Oriented

A skill should tell the AI **what to do**, not merely describe a topic.

Weak:

```text
This skill is about resumes.
```

Better:

```text
Collect the minimum required career information,
enhance the user's factual information,
validate the result,
and generate an ATS-oriented professional resume.
```

---

## 5. Do / Don't Rules

Every substantial skill should define explicit boundaries.

Example:

### Do

- Ask only for missing required information.
- Reuse information already provided.
- Validate the generated result.
- Preserve factual accuracy.
- Follow the skill's defined workflow.

### Don't

- Invent user information.
- Ask unnecessary questions.
- Ignore validation requirements.
- Override explicit user requirements without reason.

---

# 🔄 Recommended Skill Workflow

A well-designed skill should generally follow this lifecycle:

```text
┌──────────────────────┐
│     User Request     │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Understand Objective │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Collect Missing Data │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Execute Skill Logic  │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│      Validate        │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│   Quality Review     │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│      Final Output    │
└──────────────────────┘
```

Not every skill needs every stage, but the workflow should be clearly defined when applicable.

---

# 📚 Current Skill Examples

The repository can contain different categories of skills.

### 🎨 Design & UI

```text
typography-skill/
theme-style/
3d-web-experience/
```

### 🧑‍💻 Development

```text
technology-guide/
code-reviewer/
api-design/
```

### 📄 Professional Documents

```text
resume-builder/
```

Additional skills can be added as the repository grows.

---

# 📋 Skill Naming Convention

Use lowercase folder names with hyphens.

### Recommended

```text
resume-builder/
technology-guide/
typography-system/
theme-style/
3d-web-experience/
code-reviewer/
```

### Avoid

```text
ResumeBuilder/
Resume_Builder/
resume builder/
RESUME-SKILL/
```

The skill folder name should clearly describe the capability.

---

# 🔐 Quality & Safety

Skills should preserve the integrity of user-provided information.

In particular, skills should not:

- Fabricate personal information
- Invent professional experience
- Create false achievements
- Invent certifications
- Create unsupported statistics
- Claim validation that was not actually performed
- Misrepresent generated content as independently verified

When information is missing, the skill should either:

1. Ask the user for the information, or
2. Clearly identify the information as optional.

---

# 🛠️ Maintaining a Skill

When modifying an existing skill:

1. Open the skill folder.
2. Update `skill.md`.
3. Update `README.md` if the behavior or usage changed.
4. Test the skill with representative inputs.
5. Check that the instructions remain clear and non-contradictory.
6. Commit the changes.

Example:

```text
resume-builder/
├── skill.md       ← AI behavior
└── README.md      ← Human documentation
```

---

# 🤝 Contributing

Contributions are welcome.

To add a new skill:

1. Fork the repository.
2. Create a new skill folder.
3. Add `skill.md`.
4. Add `README.md`.
5. Follow the repository's skill structure and naming conventions.
6. Test the skill.
7. Commit your changes.
8. Push the branch.
9. Open a Pull Request.

Example:

```text
skills/
└── new-skill/
    ├── skill.md
    └── README.md
```

---

# 📄 License

This repository is available under the **MIT License**.

See the [`LICENSE`](LICENSE) file for details.

---

## ⭐ Vision

The long-term goal of this repository is to build a growing collection of **high-quality, reusable AI skills** that can be selected independently and applied consistently across different projects, workflows, and platforms.

```text
                    AI Skills
                       │
        ┌──────────────┼──────────────┐
        ↓              ↓              ↓
     Design       Development     Professional
        │              │              │
        ↓              ↓              ↓
   Typography     Technology      Resume Builder
   Theme          3D Experience   ...
   ...
```

**One skill → One capability → Clear instructions → Consistent results.**
