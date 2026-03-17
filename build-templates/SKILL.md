---
name: build-templates
description: Build the templates.md context file through a guided interview with a department head. Captures standard formats for recurring deliverables, naming conventions, and gold-standard examples. Use this skill when someone says "build templates," "document our formats," "standard deliverables," "template file," "naming conventions," or "what does good output look like for our team." Part of the Team Playbook system (Layer 2, File 3 of 4).
---

# Build Templates

You are interviewing a department head to build the `templates.md` file. This file defines what "good" looks like for this department's recurring deliverables. When Claude has real examples of excellent output and knows the expected format for each type of work, it produces output the team can actually use instead of generic drafts that need heavy editing.

Your tone should be detail-oriented and quality-focused. You're helping someone codify what their best work looks like so it can be replicated consistently.

## Before Starting the Interview

Ask: **"Do you have examples of deliverables your team is proud of? The ones that landed well, got great client feedback, or that you'd hold up as 'this is how we do it.' These could be emails, reports, presentations, proposals, analyses, whatever your team produces regularly. Drop them in, the more the better."**

Also read `context/department/workflows.md` if it exists, to know what deliverables the team produces.

## Interview Flow

### Section 1: Identify Recurring Deliverables
- "What are the things your team produces on a regular basis? Reports, emails, presentations, analyses, documents, whatever comes out of your department repeatedly."
- "Which of those have a specific structure or format they should always follow?"

### Section 2: Standard Formats
For each major deliverable type:
- "Walk me through the structure of a good [deliverable]. What sections does it include, in what order, and roughly how long is each section?"
- "Are there formatting rules? Things like 'always use this font,' 'never exceed one page,' 'always include a summary at the top'?"

### Section 3: Gold Standard Examples
- "Can you paste or describe an example of [deliverable] that you'd consider excellent? Something you'd want every version to look like."
- "What specifically makes this one good? What separates a great version from a mediocre one?"

### Section 4: Naming Conventions
- "Does your team follow naming conventions for files and projects? Things like date formats, client name placement, version numbering?"
- "Any folder structure standards? Where do finished deliverables go?"

### Section 5: Common Quality Issues
- "What are the most common problems you see in first drafts? The things you find yourself correcting over and over?"
- "Are there elements that people frequently forget to include?"

## After the Interview

### Output Format

```markdown
# Templates: [Department Name]

## Recurring Deliverables

### [Deliverable Type 1]
**Purpose:** [What this is for and when it's produced]
**Audience:** [Who receives this]
**Format:** [Document type, length expectations, key structural requirements]

**Standard Structure:**
1. [Section] - [What goes here, length guidance]
2. [Section] - [What goes here, length guidance]
3. [Section] - [What goes here, length guidance]

**Quality Standards:**
- [What makes this deliverable excellent]
- [Common mistakes to avoid]

**Gold Standard Example:**
> [Pasted example or detailed description of what an excellent version looks like]

---

### [Deliverable Type 2]
[Same format]

---

## Naming Conventions
| Element | Convention | Example |
|---------|-----------|---------|
| Files | [Pattern] | [Example] |
| Projects | [Pattern] | [Example] |
| Versions | [Pattern] | [Example] |

## Folder Structure
[Where deliverables are stored, organized by type or client or date]

## Common Quality Issues to Watch For
- [Issue 1]: [What goes wrong and how to prevent it]
- [Issue 2]: [What goes wrong and how to prevent it]
```

### Writing Rules
- Third person
- Real examples are more valuable than descriptions. Paste actual examples wherever possible.
- Be specific about format requirements. "Professional looking" means nothing. "12pt font, 1.15 line spacing, company logo top right, max 2 pages" is useful.
- Include anti-patterns (what NOT to do) alongside standards

## Saving the File

Save to `context/department/templates.md`.

After saving: "Templates are locked in. Last department file is tools-and-systems.md, where we document what software your team uses and how data flows between them. Say **'build tools and systems'** when you're ready."
