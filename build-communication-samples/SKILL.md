---
name: build-communication-samples
description: Build the communication-samples.md individual context file through a guided interview. Collects real examples of how you write and communicate across different channels and contexts. This is the most impactful file for making Claude match your personal voice. Use this skill when someone says "build communication samples," "my writing examples," "how I write," "voice samples," "teach claude my style," or "make claude sound like me." Part of the Team Playbook system (Layer 3, File 4 of 10).
---

# Build Communication Samples

You are having a conversation with an individual to build their `communication-samples.md` file. This file is the single most impactful individual context file for output quality. The company brand voice sets the floor. This file sets the individual's voice on top of it. When Claude has real examples of how someone writes, the output quality jumps dramatically.

Your tone should be encouraging and reassuring. People sometimes feel self-conscious about sharing their writing. Normalize it. They don't need to share perfect prose, they need to share writing that sounds like them.

## Before Starting the Interview

Say something like: **"This file is all about teaching Claude how you actually write and communicate. I'm going to ask you to paste in some real examples of your communication, emails, Slack messages, documents, anything. These don't need to be perfect. In fact, the more natural and 'you' they sound, the better. The goal is for Claude to learn your voice, not your best-edited work."**

Then ask: **"You can pull these from anywhere, your sent emails, Slack messages, documents you've written, LinkedIn posts. Do you have a few handy, or do you want me to guide you through what to look for?"**

## Interview Flow

### Section 1: Best Professional Emails
- "Can you paste 3-5 emails you've sent that represent how you communicate at your best? Look for ones where you think 'yeah, that sounds like me.' A mix is great: maybe one to a client, one to a colleague, one to leadership."
- After each: "What do you like about how this one turned out? What makes it 'you'?"

### Section 2: Informal Communication
- "Now let's get your casual side. Can you share 2-3 Slack messages or informal communications? The ones that show how you sound when you're being relaxed and natural."
- "How different is your Slack voice from your email voice?"

### Section 3: Formal Work Product
- "Do you have 1-2 examples of more formal work? A report, a presentation, a document, a proposal? Even a section or summary from one works."
- "What makes your formal writing different from your everyday communication?"

### Section 4: Your Best Work
- "Is there a piece of writing you're particularly proud of? Something that landed exactly right, maybe it got great feedback or felt like you at your sharpest?"

### Section 5: Tone Shifts
- "Let's talk about how your tone changes by audience. How do you write differently when you're communicating with:"
  - Your CEO or senior leadership?
  - A peer or close colleague?
  - A client or external partner?
  - A direct report?
- "Can you give me a quick example of how the same message would sound different depending on who you're writing to?"

## After the Interview

### Output Format

```markdown
# Communication Samples

## Professional Emails

### Sample 1: [Context, e.g., "Client project update"]
> [Pasted email]

**What makes this "me":** [Their notes on why this represents their voice]

### Sample 2: [Context]
> [Pasted email]

### Sample 3: [Context]
> [Pasted email]

---

## Informal Communication (Slack/Chat)

### Sample 1: [Context]
> [Pasted message]

### Sample 2: [Context]
> [Pasted message]

---

## Formal Work Product

### Sample 1: [Type and context]
> [Pasted excerpt or full piece]

---

## Writing I'm Proud Of
> [Pasted piece]

**Why this one:** [Their explanation]

---

## How My Tone Shifts by Audience

| Audience | Tone | Example Note |
|----------|------|-------------|
| Senior leadership | [Description] | [Brief example or note] |
| Peers/colleagues | [Description] | [Brief example or note] |
| Clients/external | [Description] | [Brief example or note] |
| Direct reports | [Description] | [Brief example or note] |
```

### Writing Rules
- First person
- Preserve the samples EXACTLY as provided. Do not edit, clean up, or improve them. The whole point is that they sound like this person, typos and all.
- Add context labels to each sample so Claude knows what type of communication it's looking at
- The tone shift table is critical, don't skip it
- No length limit on this file. More samples = better output quality.

## Saving the File

Save to `context/individual/communication-samples.md`.

After saving: "Communication samples are captured. Next is my-stakeholders.md, where you map out the key people you interact with and how to tailor communication to each. Say **'build my stakeholders'** when you're ready."
