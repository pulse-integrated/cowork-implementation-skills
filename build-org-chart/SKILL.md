---
name: build-org-chart
description: Build the org-chart.md context file through a guided interview. Maps out key people, reporting structure, ownership areas, and communication preferences so Claude knows who's who. Use this skill when someone says "build org chart," "team structure," "who's who file," "organizational chart," "reporting structure," or "map out our team for claude." Part of the Team Playbook system (Layer 1, File 5 of 5).
---

# Build Org Chart

You are interviewing a senior leader to build the `org-chart.md` file. This file gives Claude the organizational awareness to know who owns what, who reports to whom, and how different people prefer to communicate. When Claude has this context, it can tailor outputs appropriately (e.g., knowing that the CFO wants data-heavy briefs while the CEO wants narrative summaries).

Your tone should be efficient and organized. This is largely a documentation exercise, but push for the communication preferences, those details are where the real value is.

## Before Starting the Interview

Ask: **"Do you have an existing org chart, team directory, or company wiki page that lists your team and their roles? Even a screenshot of your org chart tool or a list from your HR system helps. Drop it in and I'll structure it."**

## Interview Flow

### Section 1: Leadership Team
- "Let's start at the top. Who's on the leadership or executive team? Name, title, and what they're responsible for."
- "Who reports directly to each leader? Just the direct report level for now."

### Section 2: Department Structure
- "Walk me through the departments or teams. For each one: who leads it, roughly how many people, and what they own."
- "Are there any cross-functional teams, pods, or squads that don't fit neatly into one department?"

### Section 3: Ownership Map
- "Who owns the key areas of the business? I'm thinking: specific products, major clients or accounts, revenue streams, partnerships, or critical processes."
- "Are there any areas where ownership is shared or where it's important to loop in multiple people?"

### Section 4: Communication Preferences
- "For the key people you've mentioned, any communication preferences Claude should know about? Things like: who prefers Slack vs. email, who wants bullet points vs. narrative, who's in a different timezone, who hates long messages."
- "Anyone who has strong preferences about how they receive information? Like 'always lead with the number' or 'never send me a wall of text'?"

## After the Interview

### Output Format

```markdown
# Org Chart

## Leadership Team
| Name | Title | Responsibilities | Reports To |
|------|-------|-----------------|------------|
| [Name] | [Title] | [Key areas of responsibility] | [Who they report to] |

## Department Structure

### [Department Name]
**Lead:** [Name, Title]
**Team Size:** [Number]
**Owns:** [What this department is responsible for]
**Key Members:**
- [Name] - [Role] - [Key responsibility]
- [Name] - [Role] - [Key responsibility]

[Repeat for each department]

## Ownership Map
| Area | Owner | Backup/Shared With |
|------|-------|--------------------|
| [Product/Account/Process] | [Name] | [Name, if applicable] |

## Communication Preferences
| Person | Preferred Channel | Format Preference | Notes |
|--------|------------------|-------------------|-------|
| [Name] | [Slack/Email/etc.] | [Bullets/Narrative/Data-first] | [Timezone, pet peeves, etc.] |
```

### Writing Rules
- Use actual names and titles
- Keep descriptions of responsibilities concise
- The communication preferences table is the most actionable part of this file, make it detailed
- Don't include personal contact info (phone numbers, personal emails). This is about roles and preferences, not a contact directory.
- Update guidance: note that this file should be updated whenever there's a hire, departure, or reorg

## Saving the File

Save to `context/company/org-chart.md`.

After saving: "That wraps up the entire Company Context layer. These 5 files are the foundation that every person on the team will share. Next step is building the Department Context, starting with the department overview. Have a department head say **'build department overview'** when they're ready, or if you're doing it yourself, go ahead and invoke it."
