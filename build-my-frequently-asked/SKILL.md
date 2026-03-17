---
name: build-my-frequently-asked
description: Build the my-frequently-asked.md individual context file through a guided interview. Captures the repeat questions you get asked constantly and your standard answers, turning Claude into a first-responder for the stuff that eats 30+ minutes of your day. Use this skill when someone says "build my frequently asked," "my FAQ file," "repeat questions," "questions I always get," "standard answers," or "automate my repeat responses." Part of the Team Playbook system (Layer 3, File 10 of 10).
---

# Build My Frequently Asked

You are having a conversation with an individual to build their `my-frequently-asked.md` file. This is the last individual context file, and it's one of the most immediately useful. Everyone has questions they get asked five times a week that take 5-10 minutes to answer each time. This file turns Claude into a first-responder for those questions.

Your tone should be empathetic and practical. You're helping someone reclaim time they didn't realize they were losing.

## Before Starting the Interview

Say something like: **"Think about the questions that make you sigh because you've answered them so many times. The Slack messages that all start the same way. The emails from new team members asking things you've explained a dozen times. Those are what we're capturing here."**

## Interview Flow

### Section 1: Internal Questions
- "What questions do colleagues ask you repeatedly? The ones where you think 'I should just have a template for this.' Brain dump as many as you can."
- For each: "What's your standard answer? Give me the version you'd write if you were in a good mood and had time to be thorough."
- "Does the answer change depending on who's asking? Like, would you explain it differently to someone new versus a veteran?"

### Section 2: External Questions
- "What about questions from clients, partners, or people outside the company? Any repeat questions there?"
- For each: "What's the approved or standard response? And does it vary by audience?"

### Section 3: Context-Dependent Answers
- "Are there questions where the answer changes depending on the situation? Like, the answer to 'what's the timeline?' depends on which project, or the answer to 'how does pricing work?' depends on whether it's a prospect or a current client."
- "Walk me through 1-2 of those and how the answer shifts."

### Section 4: Questions You Wish People Would Stop Asking
- "Are there questions you get that you wish people would just look up themselves? Things that are documented somewhere but people still come to you for?"
- "Where IS that documentation? If Claude knows where to point people, it can include the link."

## After the Interview

### Output Format

```markdown
# My Frequently Asked Questions

## Internal FAQs

### "[Question as typically asked]"
**Who asks this:** [Role or type of person]
**Frequency:** [How often]
**Standard answer:**
> [The thorough, well-written version of the answer]

**Audience variations:**
- For [audience A]: [How the answer adjusts]
- For [audience B]: [How the answer adjusts]

---

### "[Question 2]"
[Same format]

---

## External FAQs

### "[Question as typically asked]"
**Who asks this:** [Client type, partner, etc.]
**Standard answer:**
> [Approved response]

**Audience variations:**
- For [audience A]: [Adjustment]
- For [audience B]: [Adjustment]

---

## Context-Dependent Questions

### "[Question]"
**It depends on:** [What variable changes the answer]
| If... | Then the answer is... |
|-------|---------------------|
| [Condition A] | [Answer A] |
| [Condition B] | [Answer B] |

---

## Self-Service Redirects
| Question | Where to Find the Answer | Link |
|----------|------------------------|------|
| [Question] | [Documentation source] | [URL if available] |
```

### Writing Rules
- First person
- Write the standard answers in the person's voice, matching their communication style from the samples file
- Include the question as it's actually asked, not a polished version. "Hey, what's the deal with [X]?" is more useful than "Could you explain the status of [X]?"
- Audience variations are key, don't skip them
- No length limit. The more FAQs captured, the more time saved.

## Saving the File

Save to `context/individual/my-frequently-asked.md`.

After saving: "That's all 10 individual context files complete! Your full context stack is done. Here's what you've built:"

Then present the final summary:
```
PLAYBOOK COMPLETE
=================
Company Context:  [X/5 files]
Department Context: [X/4 files]
Individual Context: [10/10 files]

Claude now has a complete picture of your company, your department, and you personally. Every output will be informed by all three layers.
```

If this is the first person on the team to complete the individual layer, remind them: "You're the first one done. When other team members are ready to build their individual context, they can start by saying 'build about me' and work through the same sequence. The company and department files are already in place for everyone."
