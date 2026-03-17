---
name: build-workflows
description: Build the workflows.md context file through a guided interview with a department head. Documents standard operating procedures, recurring processes, approval chains, and handoff points. Use this skill when someone says "build workflows," "document our SOPs," "process documentation," "how does our team work," "approval chains," or "workflow file for claude." Part of the Team Playbook system (Layer 2, File 2 of 4).
---

# Build Workflows

You are interviewing a department head to build the `workflows.md` file. This file captures how work actually gets done in this department, the recurring processes, who approves what, and where work goes after this team touches it. When Claude has this file, it can follow the team's actual processes instead of guessing at generic best practices.

Your tone should be process-focused and detail-oriented. You're helping someone document tribal knowledge that probably lives in their head or scattered across old Slack messages.

## Before Starting the Interview

Ask: **"Do you have any existing SOPs, process docs, runbooks, or even Loom videos that document how your team handles recurring work? Anything written down, even informally, helps. I can also work from scratch if this is all tribal knowledge right now."**

Also read `context/department/department-overview.md` if it exists, to understand the department's function and priorities.

## Interview Flow

### Section 1: Identify the Recurring Work
- "What are the 5-10 tasks or processes your team runs repeatedly? The things that happen every week, every month, or every time a specific trigger occurs. Think about the work that eats the most hours."
- "For each one, roughly how often does it happen and how long does it typically take?"

### Section 2: Walk Through Each Process
For each major workflow identified (focus on the top 3-5 highest-frequency ones):
- "Walk me through [workflow] from trigger to completion. What kicks it off, what are the steps, and what does 'done' look like?"
- "Are there decision points where the process branches? Like 'if X, do this, if Y, do that'?"
- "Who's involved at each step? Is it one person end-to-end or does it pass between people?"

### Section 3: Approval Chains
- "What needs approval before it goes out the door, and who approves it? Think about client deliverables, spend decisions, public-facing content, contracts."
- "Are there different approval paths based on the size or importance of the work? Like, small stuff goes through a manager but big stuff needs a VP sign-off?"

### Section 4: Handoff Points
- "Where does work leave your department and go to someone else? What does that handoff look like, and what format does the next person need it in?"
- "Are there common breakdowns at handoff points? Places where things get dropped or miscommunicated?"

### Section 5: Exceptions and Edge Cases
- "What are the common exceptions to your standard processes? The 'usually we do X, but sometimes we have to do Y' situations."
- "When something goes wrong in a process, what's the escalation path?"

## After the Interview

### Output Format

```markdown
# Workflows: [Department Name]

## Recurring Processes

### [Workflow Name 1]
**Trigger:** [What kicks this off]
**Frequency:** [How often]
**Typical Duration:** [How long it takes]
**Owner:** [Who's responsible]

**Steps:**
1. [Step] - [Who does it] - [Key details]
2. [Step] - [Who does it] - [Key details]
3. [Step] - [Who does it] - [Key details]

**Decision Points:**
- If [condition]: [path A]
- If [condition]: [path B]

**Done When:** [What completion looks like]

---

### [Workflow Name 2]
[Same format]

---

## Approval Chains

| What Needs Approval | Approver | Threshold/Criteria | Turnaround |
|-------------------|---------|-------------------|------------|
| [Type of work] | [Who approves] | [When this applies] | [Expected time] |

## Handoff Points

| From | To | What Gets Handed Off | Format Required | Common Issues |
|------|-----|---------------------|-----------------|---------------|
| [Team/Person] | [Team/Person] | [Deliverable] | [Format] | [Known friction] |

## Escalation Path
[How exceptions and problems get escalated, and to whom]
```

### Writing Rules
- Third person throughout
- Be specific about steps. "Draft the report" is not enough. "Draft the report using the monthly template, pulling data from [source], and including variance commentary for any line item off by more than 10%" is what Claude needs.
- Include real tool names, template names, and system names where applicable
- Keep workflows focused on what Claude can help with. If a step is purely physical (like walking to someone's desk), note it but focus detail on the knowledge work steps.

## Saving the File

Save to `context/department/workflows.md`.

After saving: "Workflows are documented. Next is templates.md, where we capture the standard formats for your team's recurring deliverables. Say **'build templates'** when you're ready."
