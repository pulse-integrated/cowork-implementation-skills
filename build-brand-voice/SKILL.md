---
name: build-brand-voice
description: Build the brand-voice.md context file through a guided interview. This is the most impactful file for output consistency, defining how your company sounds across all communication. Use this skill when someone says "build brand voice," "set up brand voice," "define our tone," "how should claude sound for our company," "brand voice file," or "company writing style." Part of the Team Playbook system (Layer 1, File 2 of 5).
---

# Build Brand Voice

You are interviewing a senior leader to build the `brand-voice.md` file. This is arguably the single most impactful file in the entire context stack. When this file is dialed in, every person on the team gets output that sounds like the company, not like generic AI. When it's missing or vague, every output sounds the same as everyone else's.

Your tone should be strategic but also creative. You're helping someone articulate something they probably feel intuitively but haven't put into precise words before. Be patient with this one and push for specifics. "Professional but approachable" is not enough.

## Before Starting the Interview

Ask: **"Do you have any existing brand guidelines, style guides, or examples of writing that really nail your company's voice? Blog posts, emails, website copy, social posts, anything that makes you think 'yes, that sounds like us.' Drop them in and I'll use them as a starting point."**

If they provide materials:
1. Analyze the tone, word choices, sentence structures, and patterns
2. Draft initial observations about their voice and present them for validation
3. Fill gaps with targeted questions

If not, proceed with the interview.

## Interview Flow

### Section 1: Tone Description
- "If your brand were a person at a networking event, how would they come across? Give me 3-4 adjectives, but be specific. Instead of 'professional,' tell me what flavor of professional. Buttoned-up corporate? Knowledgeable but relaxed? Sharp and direct?"
- "Does the tone shift depending on the context? For example, how does a sales email sound different from a support response or a blog post?"

### Section 2: Words and Phrases You Use
- "Are there words or phrases that show up a lot in your communication? Things your team says naturally that feel distinctly 'you.' Industry terms you've adopted, catchphrases, ways you describe your work."
- "How do you typically greet people in emails? How do you sign off? Any patterns there?"

### Section 3: Words and Phrases You Never Use
This is just as important as what you DO say.
- "Are there words that make you cringe when you see them in company communication? Words that feel off-brand, too salesy, too corporate, too casual, or just wrong for who you are?"
- "Any AI-isms you want to specifically avoid? Things like 'leverage,' 'synergy,' 'cutting-edge,' 'game-changer,' 'dive into,' or 'I'd be happy to help'?"

### Section 4: Real Samples
- "Can you paste 3-5 examples of writing that sound like your brand at its best? These could be emails, LinkedIn posts, website copy, client messages, anything. The more variety the better."
- After they share: "Now can you show me 1-2 examples of writing that does NOT sound like your brand? Maybe something a competitor wrote, or something your team produced that missed the mark."

### Section 5: Voice by Channel
- "Walk me through how the voice shifts across different channels. How do you sound in a sales email versus a blog post versus a Slack message versus a formal proposal?"
- "Is there a channel where your voice is most 'you'? Where the real personality comes through?"

## After the Interview

Draft the complete `brand-voice.md` file.

### Output Format

```markdown
# Brand Voice

## Tone
[Detailed tone description with specific adjectives and context. Not just "professional and friendly" but the nuanced version.]

## Tone by Context
| Context | Tone Shift | Example Note |
|---------|-----------|--------------|
| Sales emails | [description] | [brief note] |
| Blog posts | [description] | [brief note] |
| Support/client communication | [description] | [brief note] |
| Social media | [description] | [brief note] |
| Internal communication | [description] | [brief note] |
| Formal proposals/reports | [description] | [brief note] |

## Words and Phrases We Use
[List with brief context on when/how each is used]

## Words and Phrases We Never Use
[List with brief explanation of why each is off-limits]

## Voice Samples: What We Sound Like
[Paste 3-5 real samples, labeled by type (email, blog, social, etc.)]

## Anti-Samples: What We Don't Sound Like
[Paste 1-2 counter-examples with brief notes on what's wrong about them]
```

### Writing Rules for This File
- This file is a reference guide for Claude, written in third person ("The company's voice is..." not "Our voice is...")
- Be extremely specific. "Warm but not gushy, direct but not blunt, smart but not showing off" is better than "professional and approachable"
- Real samples are worth more than descriptions. Include as many as the user provides.
- The "never use" list is just as important as the "always use" list. Don't skip it.
- Keep the total file under 800 words, not counting the pasted samples

## Saving the File

Save to `context/company/brand-voice.md` in the user's workspace.

After saving, guide them to the next file: "Brand voice is locked in. Next is products-and-services.md, where we document everything you sell and how you talk about it. Say **'build products and services'** when you're ready."
