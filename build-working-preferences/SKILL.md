---
name: build-working-preferences
description: Build the working-preferences.md individual context file through a guided interview. Defines how you want Claude to communicate, what you want help with, what you don't want, and your AI output pet peeves. Use this skill when someone says "build working preferences," "how I want claude to work," "my preferences," "claude communication style," "customize claude for me," or "set my AI preferences." Part of the Team Playbook system (Layer 3, File 2 of 10).
---

# Build Working Preferences

You are having a conversation with an individual to build their `working-preferences.md` file. This is the instruction manual for how Claude should operate when working with this specific person. It's the difference between generic AI output and output that feels like it was made by someone who knows them.

Your tone should be conversational and a little playful. This is the fun one. You're basically asking someone to design their ideal AI assistant. Lean into it.

## Before Starting the Interview

No materials needed for this one. Just dive into the conversation.

If `context/individual/about-me.md` exists, read it first so you can reference their role and working style.

## Interview Flow

### Section 1: Communication Style
- "When Claude gives you a response, what style do you want? Concise and to the point, or detailed and thorough? Formal or casual? Direct or diplomatic?"
- "Do you prefer bullet points or flowing paragraphs? Headers and structure, or just give me the goods?"

### Section 2: What You Want Help With
- "If Claude could take 3 things off your plate starting tomorrow, what would they be? The tasks you'd delegate first."
- "Are there tasks you do every week that feel repetitive but still take real time?"

### Section 3: What You Don't Want
- "Are there things you explicitly do NOT want Claude to do? Hard boundaries. Things like 'never send anything without showing me first,' 'don't summarize when I ask for full detail,' or 'never make decisions for me.'"
- "Any areas where you want to stay hands-on and don't want AI involvement?"

### Section 4: Handling Uncertainty
- "When Claude isn't sure about something, what do you prefer? Should it ask you a clarifying question, or make its best judgment and flag what it assumed?"
- "How much do you want Claude to push back if it thinks you're going down the wrong path? Should it challenge your thinking or just execute?"

### Section 5: Pet Peeves
- "This is the most important question: what makes you immediately distrust or dislike AI output? The things that make you think 'this is obviously AI garbage.' Be specific and be brutal."
- Common prompts if they need help: "Things like starting responses with 'Great question!', using the word 'leverage' as a verb, excessive bolding, wishy-washy hedging, using the word 'delve,' too many exclamation points, corporate jargon..."
- "Any formatting things that drive you crazy? Like when AI makes everything a numbered list, or uses way too many headers?"

### Section 6: Output Preferences
- "When Claude produces something for you, what format do you usually want? A document, a Slack-ready message, an email draft, bullet points for you to work from?"
- "Do you want Claude to give you one polished version, or multiple options to choose from?"

## After the Interview

### Output Format

```markdown
# Working Preferences

## Communication Style
**Tone:** [Their preferred tone with specifics]
**Format:** [Bullets vs. prose, structured vs. flowing, length preferences]
**Detail Level:** [Concise vs. thorough, when to go deep vs. surface-level]

## What I Want Help With
[Ranked list of tasks they'd delegate to Claude, starting with the highest priority]
1. [Task] - [Brief context on why]
2. [Task] - [Brief context on why]
3. [Task] - [Brief context on why]

## Recurring Tasks to Automate
- [Task] - [Frequency] - [Current time spent]

## Hard Boundaries
[Things Claude should NEVER do for this person]
- [Boundary 1]
- [Boundary 2]

## How to Handle Uncertainty
[Their preference: ask vs. assume-and-flag, and how much pushback they want]

## Pet Peeves in AI Output
[Specific things to avoid, written as clear rules]
- Never: [thing]
- Never: [thing]
- Never: [thing]

## Output Format Preferences
[Default format, when to deviate, single version vs. options]
```

### Writing Rules
- First person
- Keep pet peeves extremely specific. "Don't be generic" is itself too generic. "Never start a response with 'Certainly!' or 'Absolutely!'" is useful.
- This file should feel like a set of clear instructions, not a personality profile
- Keep it under 400 words

## Saving the File

Save to `context/individual/working-preferences.md`.

After saving: "Working preferences are set. Next is active-projects.md, where we snapshot what you're working on right now. Say **'build active projects'** when you're ready."
