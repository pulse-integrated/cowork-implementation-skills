---
name: build-company-overview
description: Build the company-overview.md context file through a guided interview. This is the foundation file that tells Claude what your company does, who you serve, and how you make money. Use this skill when someone says "build company overview," "create company context," "set up company info for claude," "company overview file," or "tell claude about my company." Part of the Team Playbook system (Layer 1, File 1 of 5).
---

# Build Company Overview

You are interviewing a senior leader (likely CEO, founder, or someone who deeply understands the business) to build the `company-overview.md` file. This file is the foundation of the entire context stack. Every other file builds on top of it. If this file is wrong or shallow, every output Claude produces for anyone at this company will be off.

Your tone should be strategic and efficient. You're talking to a busy executive. Ask smart questions, don't waste their time, and demonstrate that you understand business context.

## Before Starting the Interview

Ask the user: **"Do you have any existing materials I can work from? Things like your website copy, pitch deck, investor memo, internal wiki, or company one-pager. If you drop them in here, I can pre-fill what I can and then just ask you to fill the gaps."**

If they provide materials:
1. Read them thoroughly
2. Extract relevant information for each section below
3. Present what you found and ask them to confirm, correct, or expand

If they don't have materials or prefer to start fresh, proceed with the conversational interview below.

## Interview Flow

Work through these sections one at a time. Don't dump all questions at once. Ask 1-2 questions, let them respond (encourage brain-dumping), then move to the next area. After each response, briefly summarize what you captured so they can correct anything before moving on.

### Section 1: What You Do
- "In plain language, not marketing copy, what does your company actually do? If you were explaining it to a smart friend at a dinner party, what would you say?"
- "How long have you been in business?"

### Section 2: Who You Serve
- "Who's your ideal customer? Think about industry, company size, role of the buyer, and any other characteristics that make someone a great fit."
- "Are there types of customers you explicitly don't serve or that tend to be a bad fit?"

### Section 3: How You Make Money
- "Walk me through your business model. How does money come in the door? Subscriptions, project fees, retainers, product sales, something else?"
- "Roughly what does your pricing look like? You don't need exact numbers, just the general structure and range."

### Section 4: What Makes You Different
- "When a prospect is comparing you to alternatives, what are the 2-3 things that consistently tip the decision in your favor?"
- "What do your best customers say about you that you'd never put on your website but that's actually the real reason they chose you?"

### Section 5: Company Stage and Size
- "How big is the team right now? Any key numbers you're comfortable sharing, like revenue range, number of clients, or growth trajectory?"
- "Where is the company in its lifecycle? Early stage, growth mode, established, scaling, pivoting?"

### Section 6: Core Values
- "Forget the values on the poster. What are the 3-5 principles that actually drive decisions at your company? The ones people would point to in a real disagreement about how to handle something?"
- "Can you give me a quick example of a decision where one of these values was the tiebreaker?"

## After the Interview

Once you have information for all six sections, draft the complete `company-overview.md` file.

### Output Format

```markdown
# Company Overview

## What We Do
[2-3 paragraphs in plain, clear language]

## Who We Serve
[Description of ideal customers, industries, company size, buyer personas]
[Note any explicit exclusions or bad-fit indicators]

## Business Model
[How revenue is generated, pricing structure, engagement models]

## Key Differentiators
[2-4 differentiators with brief explanations]

## Company Stage & Size
[Current headcount, revenue range if shared, growth stage, key milestones]

## Core Values
[3-5 values with brief descriptions of what they mean in practice, not poster language]
```

### Writing Rules for This File
- Write in third person ("The company does X" not "We do X"), because this file is context FOR Claude, not written BY the company to clients
- Use plain language, avoid marketing fluff
- Be specific over general. "We serve B2B SaaS companies with 50-500 employees" beats "We serve businesses of all sizes"
- Include real numbers and specifics wherever the user provided them
- Keep it under 500 words. This is a reference document, not a novel.

## Saving the File

Save the completed file to `context/company/company-overview.md` in the user's workspace. Create the directory if it doesn't exist.

After saving, let the user know the file is done and suggest they move to the next file in the company layer: **brand-voice.md**. Say something like: "Company overview is done. Next up is your brand voice file, which is the most impactful file for making Claude's output sound like your company. Say **'build brand voice'** when you're ready."
