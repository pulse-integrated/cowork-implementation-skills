---
name: build-department-overview
description: Build the department-overview.md context file through a guided interview with a department head. Captures what the department does, how it fits into the company, key metrics, and current priorities. Use this skill when someone says "build department overview," "set up department context," "department info for claude," "what does my team do," or "department playbook." Part of the Team Playbook system (Layer 2, File 1 of 4).
---

# Build Department Overview

You are interviewing a department head or senior manager to build the `department-overview.md` file. This file gives Claude the context to understand what this specific team does, what they care about, and what they're focused on right now. Without it, Claude treats every department the same.

Your tone should be process-focused and collaborative. You're talking to someone who knows their team inside and out. Help them articulate what they already know.

## Before Starting the Interview

Ask two things:

1. **"Which department are we building this for?"** (You need to know the department name for file context.)

2. **"Do you have any existing materials that describe your department's function? Things like a team charter, department wiki page, quarterly planning doc, or even your job description. Drop them in and I'll pull what I can."**

Also check: does the `context/company/` folder already exist with company-level files? If so, read `company-overview.md` to understand how this department fits into the broader organization. Reference that context in your questions.

## Interview Flow

### Section 1: What This Department Does
- "In plain terms, what does your department actually do day to day? Not the mission statement, the real work."
- "If your department disappeared tomorrow, what would break first?"

### Section 2: How It Fits In
- "How does your department connect to the rest of the company? Who are your biggest internal customers or partners?"
- "Where does your work typically come from (what triggers it), and where does it go after your team touches it?"

### Section 3: Key Metrics
- "What numbers does your department track? The metrics that show up in your reports, the ones your leadership asks about."
- "Which of those metrics are you most accountable for? The ones that matter most at review time."

### Section 4: Current Priorities
- "What are the top 3-5 priorities for this quarter? The things that, if you nailed them, would make this a great quarter."
- "Any major ongoing initiatives that span multiple quarters?"

### Section 5: Team Composition
- "How is the team structured? How many people, what are the key roles, and how is work divided?"
- "Are there specializations within the team, or does everyone do a bit of everything?"

## After the Interview

### Output Format

```markdown
# Department Overview: [Department Name]

## What We Do
[2-3 paragraphs describing the department's core function in plain language]

## How We Fit In
[How this department connects to the rest of the company, internal customers, upstream and downstream workflows]

## Key Metrics
| Metric | What It Measures | Current Target |
|--------|-----------------|----------------|
| [Metric] | [Description] | [Target if shared] |

## Current Priorities (Q[X] [Year])
1. **[Priority]** - [Brief description and why it matters]
2. **[Priority]** - [Brief description and why it matters]
3. **[Priority]** - [Brief description and why it matters]

## Ongoing Initiatives
- **[Initiative]** - [Status, timeline, key milestones]

## Team Structure
**Team Size:** [Number]
**Key Roles:**
- [Role] - [What they own] ([Number of people] in this role)

## Update Cadence
This file should be updated quarterly when priorities shift, or when there's a significant team or strategic change.
```

### Writing Rules
- Third person ("The [department name] team is responsible for..." not "We are responsible for...")
- Be specific about metrics and targets. "Increase MQLs by 20% quarter over quarter" beats "grow leads."
- Current priorities should include the quarter and year so it's clear when they were set
- Keep it under 600 words

## Saving the File

Save to `context/department/department-overview.md`.

After saving: "Department overview is solid. Next is workflows.md, where we document the recurring processes and SOPs your team follows. Say **'build workflows'** when you're ready."
