---
name: build-my-stakeholders
description: Build the my-stakeholders.md individual context file through a guided interview. Maps the key people you interact with and how to tailor communication to each one. Use this skill when someone says "build my stakeholders," "who do I work with," "my contacts file," "stakeholder map," "communication by person," or "tailor emails by recipient." Part of the Team Playbook system (Layer 3, File 5 of 10).
---

# Build My Stakeholders

You are having a conversation with an individual to build their `my-stakeholders.md` file. This file maps the key people this person interacts with and, critically, how to tailor communication to each of them. When Claude has this file, every email, report, or document it drafts is already adjusted for the recipient without the person having to specify it each time.

Your tone should be conversational and a bit strategic. You're helping someone think about their relationships and communication patterns in a structured way.

## Before Starting the Interview

Ask: **"Think about the people you interact with most at work, both inside and outside the company. I'm going to ask about each of them, not just who they are, but how they like to receive information and any quirks Claude should know about."**

## Interview Flow

### Section 1: Internal Stakeholders
- "Who are the 3-5 people inside the company you interact with most? Manager, direct reports, cross-functional partners, whoever."
- For each person:
  - "What do they care about most? What's top of mind for them?"
  - "How do they prefer to receive information? Data-heavy or narrative? Detailed or executive summary? Quick bullets or full context?"
  - "Any communication quirks? Things like 'my CEO hates long emails,' 'my VP wants options not recommendations,' 'my manager needs the bottom line first.'"

### Section 2: External Stakeholders
- "Who are the key people outside the company you communicate with regularly? Clients, partners, vendors."
- For each:
  - "What's the nature of the relationship? What do they care about?"
  - "How do you typically communicate with them? What tone do you use?"
  - "Any context Claude should know? Things like 'this client is detail-oriented,' 'this vendor needs to be managed firmly,' 'this partner is very formal.'"

### Section 3: Approval Chains
- "For the work you produce, who needs to sign off on what? Walk me through who approves different types of output."
- "What do those approvers typically look for? What makes them send something back for revision?"

## After the Interview

### Output Format

```markdown
# My Stakeholders

## Internal Stakeholders

### [Name] - [Title]
**Relationship:** [Manager/Direct report/Peer/Cross-functional partner]
**What they care about:** [Top priorities and concerns]
**Communication preference:** [How they want to receive information]
**Quirks:** [Specific things to know about communicating with them]
**When I typically interact:** [Context: weekly 1:1, project reviews, etc.]

### [Name] - [Title]
[Same format]

---

## External Stakeholders

### [Name/Company] - [Role]
**Relationship:** [Client/Partner/Vendor]
**What they care about:** [Key concerns and priorities]
**Communication tone:** [How to communicate with them]
**Context:** [Relationship background, preferences, sensitivities]

### [Name/Company] - [Role]
[Same format]

---

## Approval Chains

| Type of Work | Approver | What They Look For | Common Revision Reasons |
|-------------|---------|-------------------|----------------------|
| [Work type] | [Name] | [Their criteria] | [Why they send things back] |
```

### Writing Rules
- First person
- Be specific about communication preferences. "Prefers concise" is okay. "Never send her more than 3 bullet points in Slack, she won't read past that" is great.
- Include enough context that Claude could draft a message TO any of these people and get the tone right
- Update this file when key relationships change
- Keep it under 600 words

## Saving the File

Save to `context/individual/my-stakeholders.md`.

After saving: "Stakeholders are mapped. Next is my-writing-voice.md, where we define the rules behind how you write, complementing the communication samples you already provided. Say **'build my writing voice'** when you're ready."
