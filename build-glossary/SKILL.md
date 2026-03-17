---
name: build-glossary
description: Build the glossary.md context file through a guided interview. Captures internal acronyms, industry jargon, project codenames, and client shorthand so Claude understands how your team actually talks. Use this skill when someone says "build glossary," "internal terms," "acronyms file," "jargon list," "company terminology," or "define our shorthand for claude." Part of the Team Playbook system (Layer 1, File 4 of 5).
---

# Build Glossary

You are interviewing a senior leader to build the `glossary.md` file. This file prevents Claude from misinterpreting internal language. Every company develops its own vocabulary, and without this file, Claude either guesses wrong or uses generic industry terms instead of the team's actual language.

Your tone should be efficient and organized. This is more of a cataloging exercise than a deep strategic interview. Move quickly, capture everything, and organize it cleanly.

## Before Starting the Interview

Ask: **"Do you have any existing glossaries, onboarding docs, or internal wikis that define terms your team uses? Even a Slack message where someone explained an acronym to a new hire would help. Drop anything you have in here."**

## Interview Flow

### Section 1: Internal Acronyms
- "What acronyms does your team use daily that an outsider wouldn't know? Think about ones that show up in Slack, meetings, or reports. Just brain-dump them, I'll organize after."
- Probe for common categories: department names, processes, tools, metrics, report names

### Section 2: Industry Jargon
- "What industry-specific terms does your team use that are standard in your field but might not be obvious to someone outside it?"
- "Are there terms your team uses differently than the rest of the industry? Places where your definition is specific to how you operate?"

### Section 3: Project Codenames
- "Do you use codenames for projects, initiatives, or internal efforts? Things that wouldn't make sense to someone who just joined."
- "Any recurring project naming conventions? Like naming projects after cities, or using a specific prefix?"

### Section 4: Client and Partner Shorthand
- "Do you refer to clients by abbreviations or nicknames internally? Like calling 'Acme Corporation' just 'Acme' or 'AC'?"
- "Any vendor or partner shorthand the team uses?"

### Section 5: Catch-All
- "Anything else that would confuse a new employee on their first day? Terms, phrases, inside references that have become part of how the team communicates?"

## After the Interview

### Output Format

```markdown
# Glossary

## Internal Acronyms
| Term | Meaning | Context |
|------|---------|---------|
| [Acronym] | [Full meaning] | [When/where it's used] |

## Industry Terms
| Term | Definition | Our Usage |
|------|-----------|-----------|
| [Term] | [Standard definition] | [How we specifically use it, if different] |

## Project Codenames
| Codename | Refers To | Status |
|----------|----------|--------|
| [Name] | [What it actually is] | [Active/Completed/Planned] |

## Client & Partner Shorthand
| Shorthand | Full Name | Notes |
|-----------|----------|-------|
| [Short] | [Full name] | [Any relevant context] |

## Other Internal Language
[Catch-all for anything that doesn't fit above categories]
```

### Writing Rules
- Third person reference format
- Keep definitions concise, one line each where possible
- Include context/usage notes so Claude knows when to use each term
- This file should be easy to scan. Tables are better than paragraphs here.
- Mark project codenames with status so Claude knows what's current vs. historical

## Saving the File

Save to `context/company/glossary.md`.

After saving: "Glossary is captured. Last company file is the org chart, where we map out who's who and who owns what. Say **'build org chart'** when you're ready."
