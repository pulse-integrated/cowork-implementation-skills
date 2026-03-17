---
name: build-my-goals-and-kpis
description: Build the my-goals-and-kpis.md individual context file through a guided interview. Captures what you're measured on, how you're tracking, and what success looks like so Claude can orient outputs toward your actual goals. Use this skill when someone says "build my goals and KPIs," "my metrics," "what I'm measured on," "OKRs file," "performance goals," or "success metrics for claude." Part of the Team Playbook system (Layer 3, File 7 of 10).
---

# Build My Goals and KPIs

You are having a conversation with an individual to build their `my-goals-and-kpis.md` file. When Claude knows what success looks like for someone, every output gets subtly oriented toward those outcomes. A sales rep's drafts lean toward pipeline impact. A marketer's outputs lean toward conversion. Without this file, Claude optimizes for generic "good."

Your tone should be direct and goal-oriented. You're helping someone get clear about what they're actually being measured on.

## Before Starting the Interview

Ask: **"Do you have your current OKRs, goals, or performance plan written down somewhere? A performance review template, a goal-setting doc, or even what your manager shared in your last 1:1? Drop it in if you have it."**

## Interview Flow

### Section 1: Performance Framework
- "What performance framework does your company use? OKRs, KPIs, quotas, MBOs, or something more informal?"
- "How often are goals set and reviewed? Quarterly, annually, ongoing?"

### Section 2: Your Current Goals
- "What are your current goals? Walk me through each one."
- For each: "How is this measured? What's the specific metric or outcome?"
- "How are you tracking against each one right now? Ahead, on track, behind?"

### Section 3: What Your Manager Cares About
- "When your manager evaluates your performance, what do they weight most heavily? What's the thing that really moves the needle in their eyes?"
- "Is there a difference between the formal goals and what actually gets you noticed or promoted?"

### Section 4: Connection to Bigger Picture
- "How do your individual goals connect to your department's goals? And to the company's objectives?"
- "Are there company-level metrics that your work directly impacts, even if you're not formally measured on them?"

### Section 5: Exceeding vs. Meeting
- "What's the difference between 'meeting expectations' and 'exceeding expectations' in your role? What separates good from great?"
- "If you could overachieve on one goal this quarter, which one would have the biggest impact on your career?"

## After the Interview

### Output Format

```markdown
# My Goals and KPIs

## Performance Framework
[What system the company uses, review cadence]

## Current Goals (Q[X] [Year])

### Goal 1: [Goal Name]
**Metric:** [How it's measured]
**Target:** [Specific target]
**Current Status:** [Ahead/On Track/Behind]
**Notes:** [Any context on trajectory or blockers]

### Goal 2: [Goal Name]
[Same format]

### Goal 3: [Goal Name]
[Same format]

## What My Manager Cares About Most
[The 1-2 things that carry the most weight in evaluations]

## The Informal Metrics
[Things that aren't formally tracked but matter for visibility, promotion, or reputation]

## How My Goals Connect Up
| My Goal | Department Goal | Company Goal |
|---------|----------------|-------------|
| [Individual] | [Department] | [Company] |

## Meeting vs. Exceeding Expectations
**Meeting:** [What "good enough" looks like]
**Exceeding:** [What "crushing it" looks like]

## Highest-Impact Goal
[The one goal where overachievement would matter most, and why]
```

### Writing Rules
- First person
- Include specific numbers wherever possible. "Grow pipeline" is vague. "Add $500K in qualified pipeline this quarter" is actionable.
- Include the quarter and year so goals are clearly time-stamped
- The "informal metrics" section matters, help them articulate the unspoken success factors
- Keep it under 400 words

## Saving the File

Save to `context/individual/my-goals-and-kpis.md`.

After saving: "Goals and KPIs are captured. Next is my-meeting-cadence.md, where we map your recurring meetings so Claude can help with prep and follow-up. Say **'build my meeting cadence'** when you're ready."
