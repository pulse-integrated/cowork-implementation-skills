---
name: build-my-tools-and-logins
description: Build the my-tools-and-logins.md individual context file through a guided interview. Captures your personal tool workflow, where you draft vs. finalize, file naming habits, and notification preferences. Use this skill when someone says "build my tools and logins," "my tool workflow," "how I use my tools," "personal tech stack," "where I work," or "my software file." Part of the Team Playbook system (Layer 3, File 9 of 10).
---

# Build My Tools and Logins

You are having a conversation with an individual to build their `my-tools-and-logins.md` file. This file captures how this specific person uses their tools, not just what tools they have access to (that's in the department file), but their personal workflow patterns. When Claude knows someone drafts in Google Docs, gets feedback in Notion, and shares via Slack, it formats output accordingly.

Your tone should be practical and quick. This is a workflow inventory, not a deep strategic conversation.

## Before Starting the Interview

Ask: **"This one's pretty quick. I just need to understand how YOU personally use your tools, where you draft things, where you finalize them, and how you share them. Ready to walk through it?"**

Read `context/department/tools-and-systems.md` if it exists, so you already know what tools the team uses. Focus on how this individual uses them specifically.

## Interview Flow

### Section 1: Primary Tools
- "Walk me through the tools you live in daily. Group them by how you use them:"
  - Communication (Slack, email, etc.)
  - Documentation (Google Docs, Notion, Word, etc.)
  - Project management (ClickUp, Asana, etc.)
  - File storage (Google Drive, Dropbox, etc.)
  - Anything else you touch daily

### Section 2: Workflow Patterns
- "When you create something, where do you start? Where do you draft, where do you get feedback, and where does the final version end up?"
- "Give me a specific example. Like, when you write a report, what's the journey from blank page to delivered?"

### Section 3: File and Naming Habits
- "Do you follow any file naming conventions? Or do you have your own system?"
- "How do you organize your folders? Any structure you maintain?"

### Section 4: Notification and Triage
- "How do you triage incoming requests? Do you live in your inbox, Slack, or a project management tool?"
- "What's your notification strategy? Everything on, selectively filtered, or mostly off?"

### Section 5: Output Format Preferences
- "When Claude creates something for you, what format should it be in by default? Google Doc, Word file, Slack-ready text, email draft, markdown?"
- "Does this change depending on the type of work?"

## After the Interview

### Output Format

```markdown
# My Tools and Logins

## Daily Tools
| Category | Tool | How I Use It |
|----------|------|-------------|
| Communication | [Tool] | [Specific usage pattern] |
| Documentation | [Tool] | [Specific usage pattern] |
| Project Management | [Tool] | [Specific usage pattern] |
| File Storage | [Tool] | [Specific usage pattern] |
| Other | [Tool] | [Specific usage pattern] |

## My Workflow Pattern
**Draft in:** [Tool/platform]
**Get feedback in:** [Tool/platform]
**Finalize in:** [Tool/platform]
**Share via:** [Tool/platform]

**Example workflow:** [Specific example of how a piece of work moves through their tools]

## File Naming Conventions
[Their naming patterns, or "No consistent convention"]

## Folder Structure
[How they organize their files, or "No strict structure"]

## Notification & Triage
**Primary inbox:** [Where incoming requests land]
**Triage method:** [How they prioritize and process]
**Notification level:** [High/Selective/Minimal]

## Default Output Formats for Claude
| Work Type | Preferred Format | Notes |
|-----------|-----------------|-------|
| [Type] | [Format] | [Any specifics] |
```

### Writing Rules
- First person
- Focus on workflow patterns, not just tool names
- Don't include passwords, tokens, or credentials. Just workflow context.
- This file helps Claude know what format to produce output in, make the output format table specific

## Saving the File

Save to `context/individual/my-tools-and-logins.md`.

After saving: "Almost there. Last file is my-frequently-asked.md, where we capture the repeat questions you get and your standard answers. Say **'build my frequently asked'** when you're ready."
