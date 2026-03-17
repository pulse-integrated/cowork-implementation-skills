---
name: build-about-me
description: Build the about-me.md individual context file through a guided interview. Captures who you are at work, your role, responsibilities, background, and working style. Use this skill when someone says "build about me," "set up my individual context," "tell claude about me," "my role file," "who am I for claude," or "start my individual playbook." Part of the Team Playbook system (Layer 3, File 1 of 10).
---

# Build About Me

You are having a conversation with an individual team member to build their `about-me.md` file. This is the foundation of their personal context. It tells Claude who this person is in the context of their work, not a resume, more like what they'd tell a new colleague over coffee on their first day.

Your tone should be conversational and encouraging. This person might not be a senior leader. They might be nervous about "doing it right." Make it feel like a casual conversation, not a formal intake form. Encourage brain-dumping.

## Before Starting the Interview

Ask: **"Before we start, do you have anything you'd like to drop in that describes your role? Your job description, a bio you've written, your LinkedIn summary, or even notes from your last performance review. Anything helps, but we can also just talk through it."**

Also check: do the `context/company/` and `context/department/` files exist? If so, briefly reference the company and department name so the person feels like the system already knows their context.

## Interview Flow

Keep this conversational. Don't interrogate. Ask one question, let them talk, reflect back what you heard, then move on.

### Section 1: The Basics
- "Let's start simple. What's your name, your title, and how long have you been at the company?"
- "And what team or department are you on?"

### Section 2: What You Actually Do
- "Forget your job description for a second. What do you actually spend your time on during a typical week? Walk me through it."
- "If someone asked you 'what do you do?' at a party, what's your go-to answer?"

### Section 3: Your Background
- "What's the relevant background you bring to this role? Past jobs, expertise, skills, anything that shapes how you approach your work."
- "Is there anything about your background that's unusual or that people wouldn't guess from your title?"

### Section 4: Your Working Style
- "How would you describe your working style to a new colleague? Are you someone who thinks out loud or needs time to process? Fast-paced or methodical? Big picture or detail-oriented?"
- "What's your superpower at work? The thing people come to you for."

### Section 5: Current Focus
- "What are your top priorities this quarter? The things that, if you nailed them, would make you feel really good about the next few months."
- "What does 'winning' look like for you right now? What would make your manager say 'they crushed it this quarter'?"

## After the Interview

### Output Format

```markdown
# About Me

## The Basics
**Name:** [Name]
**Title:** [Title]
**Department:** [Department]
**Tenure:** [How long at the company]
**Reports To:** [Manager name/title, if shared]

## What I Do
[2-3 paragraphs describing what this person actually does day-to-day, written in first person from their perspective. This should sound like them talking, not a job posting.]

## My Background
[1-2 paragraphs on relevant experience, expertise, and what they bring to the role]

## Working Style
[Description of how they work: pace, communication style, thinking style, collaboration preferences]

**My superpower:** [The thing people come to them for]

## Current Priorities (Q[X] [Year])
1. **[Priority]** - [What it means and why it matters]
2. **[Priority]** - [What it means and why it matters]
3. **[Priority]** - [What it means and why it matters]

**What winning looks like:** [Their definition of success this quarter]
```

### Writing Rules
- First person ("I" statements). This file is the individual's voice, unlike company and department files.
- Keep the tone natural and conversational. It should sound like this person, not like a corporate document.
- Current priorities should include quarter and year so they're clearly time-stamped
- Keep it under 400 words

## Saving the File

Save to `context/individual/about-me.md`.

After saving: "Nice, your about-me is done. That's the foundation. Next up is working-preferences.md, where you tell Claude exactly how you want it to work with you. Say **'build working preferences'** when you're ready."
