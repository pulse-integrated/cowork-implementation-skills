---
name: build-tools-and-systems
description: Build the tools-and-systems.md context file through a guided interview with a department head. Documents what software the team uses, how data flows between systems, and integration points. Use this skill when someone says "build tools and systems," "document our tech stack," "what software does my team use," "tool inventory," "systems file," or "integrations map." Part of the Team Playbook system (Layer 2, File 4 of 4).
---

# Build Tools and Systems

You are interviewing a department head to build the `tools-and-systems.md` file. This file maps the department's technology landscape so Claude understands where data lives, how systems connect, and what format outputs need to be in. When someone says "pull the latest numbers," Claude needs to know which system those numbers live in.

Your tone should be practical and systematic. You're building an inventory with workflow context, not just a list of software.

## Before Starting the Interview

Ask: **"Do you have a list of tools your team uses? Maybe from an IT inventory, an onboarding checklist, or a 'tools we use' page in your wiki? Even a quick brain dump works."**

## Interview Flow

### Section 1: Core Tools by Category
- "Let's walk through the tools your team uses by category. Start with the ones your team lives in daily:"
  - Communication (Slack, Teams, email client)
  - Project management (ClickUp, Asana, Jira, Monday)
  - Documentation (Google Docs, Notion, Confluence)
  - File storage (Google Drive, Dropbox, SharePoint)
  - CRM or customer data (Salesforce, HubSpot)
  - Analytics or reporting (Google Analytics, Tableau, Looker)
  - Department-specific tools (design: Figma, dev: GitHub, finance: QuickBooks, etc.)
  - Any other tools unique to this team

### Section 2: How Data Flows
- "How do these tools connect? Walk me through a typical piece of work and which systems it touches along the way."
- "Are there manual steps where someone has to copy data from one system to another? Those are important to know about."

### Section 3: Access and Permissions
- "Are there different access levels within your team? Like some people can edit in [tool] but others are view-only?"
- "Any tools that require special access, training, or approval to use?"

### Section 4: Integration Points
- "Which of your tools talk to each other automatically? Things like Slack notifications from project management, or CRM syncing to your email platform."
- "Are there integrations you wish you had but don't?"

### Section 5: Pain Points
- "Where are the biggest friction points in your toolset? Tools that don't talk to each other, clunky workarounds, things the team complains about."
- "If you could wave a magic wand and fix one tool or workflow issue, what would it be?"

## After the Interview

### Output Format

```markdown
# Tools and Systems: [Department Name]

## Core Tools

### Communication
| Tool | Purpose | Used By | Notes |
|------|---------|---------|-------|
| [Tool] | [What it's used for] | [Everyone/Subset] | [Key details] |

### Project Management
| Tool | Purpose | Used By | Notes |
|------|---------|---------|-------|

### Documentation & Storage
| Tool | Purpose | Used By | Notes |
|------|---------|---------|-------|

### Analytics & Reporting
| Tool | Purpose | Used By | Notes |
|------|---------|---------|-------|

### Department-Specific
| Tool | Purpose | Used By | Notes |
|------|---------|---------|-------|

## Data Flow
[Describe how a typical piece of work moves through the system stack, which tools it touches and in what order]

## Integrations
| From | To | What Syncs | Trigger |
|------|-----|-----------|---------|
| [Tool A] | [Tool B] | [What data moves] | [Auto/Manual/Scheduled] |

## Access Notes
| Tool | Access Levels | How to Get Access |
|------|--------------|-------------------|
| [Tool] | [Admin/Editor/Viewer] | [Process] |

## Known Pain Points
- [Pain point 1]: [Description and current workaround]
- [Pain point 2]: [Description and current workaround]
```

### Writing Rules
- Third person
- Include specific tool names, not generic categories
- Note whether integrations are automatic, manual, or scheduled
- Don't include passwords, API keys, or sensitive credentials. This is about workflow context, not access management.
- Flag tools that Claude can connect to via MCP or native integrations, this helps teams prioritize their Cowork setup

## Saving the File

Save to `context/department/tools-and-systems.md`.

After saving: "That wraps up the Department Context layer. Your team now has both company-wide and department-specific context in place. Next step is the Individual Context layer, where each team member personalizes Claude for themselves. Have each person say **'build about me'** to start their individual setup."
