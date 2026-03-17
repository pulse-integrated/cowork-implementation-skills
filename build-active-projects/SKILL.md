---
name: build-active-projects
description: Build the active-projects.md individual context file through a guided interview. Captures current projects, statuses, deadlines, collaborators, and blockers. This is a living file that should be updated weekly. Use this skill when someone says "build active projects," "what am I working on," "my projects file," "current work," "project tracker for claude," or "update my projects." Part of the Team Playbook system (Layer 3, File 3 of 10).
---

# Build Active Projects

You are having a conversation with an individual to build their `active-projects.md` file. This is a living snapshot of what they're working on right now. Unlike most context files that update quarterly, this one should be refreshed weekly. When Claude knows what's on someone's plate, it can proactively connect the dots between tasks, flag deadline conflicts, and tailor outputs to the right project context.

Your tone should be organized and efficient. This is more of a structured capture than a deep interview. Help them get it all out of their head and into a clean format.

## Before Starting the Interview

Ask: **"Do you have a project management tool (ClickUp, Asana, Jira, Monday) or a task list you could share or paste from? Even a screenshot of your current task board helps. I can structure it from there."**

Read `context/individual/about-me.md` if it exists for priority context.

## Interview Flow

### Section 1: Current Project Inventory
- "Let's get everything on the table. What are all the projects you're actively working on right now? Don't filter, just list everything, big and small."
- For each: "What's the status? Not started, in progress, blocked, or wrapping up?"

### Section 2: Details Per Project
For each project (start with the highest priority ones):
- "What's the deadline or key milestone coming up?"
- "Who else is involved, and what are their roles on this project?"
- "Any blockers or open questions that need to be resolved?"
- "Where do the relevant files, briefs, or resources live?"

### Section 3: Pipeline
- "What's coming next? Projects that haven't started yet but are on the horizon."
- "Any projects that are winding down that I should note as nearly complete?"

### Section 4: Time Allocation
- "Roughly, how is your time split across these projects? Like, 'Project A takes 40% of my week, Project B is 20%,' etc."

## After the Interview

### Output Format

```markdown
# Active Projects

*Last updated: [Date]*

## In Progress

### [Project Name]
**Status:** In Progress
**Priority:** [High/Medium/Low]
**Deadline:** [Date or milestone]
**My Role:** [What this person does on this project]
**Collaborators:**
- [Name] - [Their role on this project]
**Current Focus:** [What they're working on this week for this project]
**Blockers:** [Any blockers, or "None"]
**Resources:** [Links or file locations for key documents]

---

### [Project Name 2]
[Same format]

---

## Not Yet Started

### [Project Name]
**Expected Start:** [Date or trigger]
**Brief:** [1-2 sentences on what it is]

## Wrapping Up

### [Project Name]
**Status:** Finalizing
**Remaining:** [What's left to do]

## Time Allocation
| Project | % of Week | Notes |
|---------|----------|-------|
| [Project] | [%] | [Any context] |

---

*This file should be updated weekly. Quick update: review each project, adjust status, update current focus, and add/remove projects as needed.*
```

### Writing Rules
- First person
- Include the "last updated" date prominently at the top
- Sort by priority within each status group
- Keep project descriptions brief, this is a reference doc, not project documentation
- Include a reminder at the bottom that this file needs weekly updates

## Saving the File

Save to `context/individual/active-projects.md`.

After saving: "Projects are captured. Next is communication-samples.md, which is the single most impactful file for making Claude sound like YOU. Say **'build communication samples'** when you're ready."
