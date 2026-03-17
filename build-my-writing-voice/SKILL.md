---
name: build-my-writing-voice
description: Build the my-writing-voice.md individual context file through a guided interview. Defines the rules behind how you write, your word choices, sentence patterns, and style influences. Complements communication-samples.md by explaining WHY you sound the way you do. Use this skill when someone says "build my writing voice," "my writing rules," "personal style guide," "how I write," "writing patterns," or "voice rules." Part of the Team Playbook system (Layer 3, File 6 of 10).
---

# Build My Writing Voice

You are having a conversation with an individual to build their `my-writing-voice.md` file. While `communication-samples.md` shows Claude what the output should look like, this file tells Claude the rules behind why it sounds that way. Think of samples as the "what" and this file as the "how."

Your tone should be thoughtful and probing. Most people have never articulated their writing rules explicitly. You're helping them discover patterns they follow instinctively.

## Before Starting the Interview

If `context/individual/communication-samples.md` exists, read it first. You can reference specific patterns you notice in their writing to prompt deeper reflection.

Say: **"I'm going to help you articulate the unwritten rules of how you write. Most people have a consistent style but have never put it into words. I'll ask some questions and also point out patterns I might notice."**

## Interview Flow

### Section 1: Word Choices
- "Are there words or phrases you use a lot? Things that just naturally come out when you write?"
- "What about words you'd never use? Words that feel wrong or off-brand for you personally?"
- "Any words you catch yourself overusing that you want Claude to moderate?"

### Section 2: Sentence Structure
- "Are you a short-and-punchy writer, or do you tend toward longer, more complex sentences? Or does it depend on context?"
- "Do you lean toward active voice or passive voice? Direct statements or more nuanced, hedged language?"

### Section 3: Openings and Closings
- "How do you typically open an email? Any go-to opening lines or patterns?"
- "How do you close? Standard sign-offs, or does it vary?"
- "What about documents or reports? How do you typically start and end those?"

### Section 4: Voice by Channel
- "Walk me through how your writing shifts across channels:"
  - Slack (casual)
  - Email (professional)
  - Reports or documents (formal)
  - Presentations (concise)
- "Where does your personality come through most?"

### Section 5: Style Influences
- "Are there writers, communicators, or leaders whose style you admire or try to emulate? Not that you're copying them, but whose communication approach resonates with you?"
- "What is it about their style that you connect with?"

### Section 6: The Unwritten Rules
If you've read their communication samples, point out patterns:
- "I noticed in your samples that you tend to [pattern]. Is that intentional?"
- "You seem to [pattern] in informal communication but [different pattern] in formal. Is that a conscious shift?"

## After the Interview

### Output Format

```markdown
# My Writing Voice

## Words I Use
[List of words and phrases that are part of their natural vocabulary]

## Words I Never Use
[List with brief notes on why, e.g., "leverage (too corporate), synergy (meaningless), deep dive (overused)"]

## Sentence Style
[Description of their typical sentence structure, length, and complexity patterns]

## Active vs. Passive
[Their tendency and when it shifts]

## How I Open and Close

### Emails
**Openings:** [Typical patterns]
**Closings:** [Typical sign-offs]

### Documents/Reports
**Openings:** [How they start formal work]
**Closings:** [How they wrap up]

### Slack/Chat
**Typical style:** [How they sound in informal channels]

## Voice by Channel
| Channel | Style Notes |
|---------|------------|
| Slack | [Description] |
| Email | [Description] |
| Documents/Reports | [Description] |
| Presentations | [Description] |

## Style Influences
[Who they admire and what about their style resonates]

## Unwritten Rules
[Patterns identified from samples and conversation, written as clear rules for Claude to follow]
- [Rule 1]
- [Rule 2]
- [Rule 3]
```

### Writing Rules
- First person
- This file should read like a style guide, clear rules Claude can follow
- The difference between this and communication-samples: samples show the output, this file explains the rules. Both are needed.
- Be specific. "I write casually" is useless. "I use contractions, start sentences with 'And' or 'But,' and rarely use semicolons" is useful.
- Keep it under 500 words

## Saving the File

Save to `context/individual/my-writing-voice.md`.

After saving: "Writing voice is defined. Next is my-goals-and-kpis.md, where we capture what you're measured on so Claude can orient everything toward your success metrics. Say **'build my goals and KPIs'** when you're ready."
