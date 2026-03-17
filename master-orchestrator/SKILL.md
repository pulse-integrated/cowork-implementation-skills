---
name: team-playbook
description: Master orchestrator skill for Claude Cowork team deployments. This skill runs through all 19 context sub-skills in sequence to give Claude full organizational, departmental, and individual context before executing any task. Use this skill at the start of EVERY Cowork session, for ANY task type, regardless of department or role. This skill should trigger on every single user interaction because it is the foundation that makes all other skills work. If you are in a workspace that contains a team-playbook folder, always run this skill first.
---

# Team Playbook Orchestrator

This is the master orchestrator for your Claude Cowork workspace. Before executing any task, run through each sub-skill below in sequence. This ensures Claude has full context about the company, the department, and the individual before producing any output.

Do not skip layers. Do not jump ahead to the task. Run the full sequence every session.

## How This Works

The workspace is organized into three context layers and a skills layer. Each layer builds on the one before it. The orchestrator reads them in order so that Claude operates with the same foundational understanding every time, regardless of who is using it or what they're asking for.

**Layer 1: Company Context** (shared by everyone in the organization)
**Layer 2: Department Context** (shared by everyone on a specific team)
**Layer 3: Individual Context** (unique to each person)
**Layer 4: Task Execution** (routes to the appropriate department or individual skill file)

## Sequence

### Step 1: Load Company Context

Read the following 5 files from `context/company/` in this order. These define how Claude understands the business. Every output should be consistent with what's in these files.

1. **`context/company/company-overview.md`**
   Read first. This tells you what the company does, who it serves, how it makes money, and what makes it different. This is the lens through which every piece of work should be framed.

2. **`context/company/brand-voice.md`**
   Read second. This defines how the company sounds. Tone, language, words to use, words to never use, and how voice shifts by context. All written output must comply with these rules unless the individual's voice file explicitly overrides for a specific context.

3. **`context/company/products-and-services.md`**
   Read third. This is how the company describes what it sells. Use this language exactly when referencing products or services. Do not paraphrase product names, descriptions, or positioning unless instructed.

4. **`context/company/glossary.md`**
   Read fourth. These are the internal acronyms, jargon, project codenames, and shorthand the company uses. Apply these throughout all output. If a term appears in the glossary, use the company's definition, not a generic one.

5. **`context/company/org-chart.md`**
   Read fifth. This tells you who's who, the reporting structure, department ownership, and communication preferences. Reference this when the task involves other people in the organization.

**After reading all 5 company files:** You now have the company foundation. Every output from this point forward should be consistent with the company's voice, terminology, products, and organizational structure.

---

### Step 2: Load Department Context

Read the following 4 files from `context/department/` in this order. These define how the user's specific team operates within the company.

6. **`context/department/department-overview.md`**
   What this department does, how it fits into the company, key metrics it tracks, and current quarter priorities. Frame all output within the department's objectives.

7. **`context/department/workflows.md`**
   Standard operating procedures, step-by-step processes, approval chains, and handoff points. Follow these workflows when executing tasks. Do not create ad hoc processes when a documented workflow exists.

8. **`context/department/templates.md`**
   Standard formats for recurring deliverables, naming conventions, and examples of work done well. Match these formats unless the user explicitly requests something different.

9. **`context/department/tools-and-systems.md`**
   What software and platforms this department uses, how data flows between systems, and integration points. Produce output in formats compatible with these tools.

**After reading all 4 department files:** You now have the department layer. Output should follow this department's workflows, templates, and tool conventions.

---

### Step 3: Load Individual Context

Read the following 10 files from `context/individual/` in this order. These define how the specific user works, communicates, and wants Claude to operate.

10. **`context/individual/about-me.md`**
    Who this person is, what they're responsible for, their background, and current priorities. Tailor output to their role and focus areas.

11. **`context/individual/working-preferences.md`**
    How this person wants Claude to communicate, output format preferences, what they want help with, what they do NOT want Claude to do, and their pet peeves. Follow these rules strictly. If this file says "never start with a question," never start with a question. If it says "always give me the answer first, then the reasoning," do that.

12. **`context/individual/active-projects.md`**
    Current projects, deadlines, collaborators, blockers, and what's coming next. Reference this when the user mentions a project by name or asks about status. If a task relates to an active project, connect it to the relevant context automatically.

13. **`context/individual/communication-samples.md`**
    Real examples of how this person writes. This is the calibration file. When producing written output, match the tone, sentence structure, and style demonstrated in these samples. This file takes precedence over brand-voice.md for individual-attributed output (emails from this person, Slack messages, etc.). Brand voice still applies to company-attributed output (blog posts, marketing materials, etc.).

14. **`context/individual/my-stakeholders.md`**
    Who this person interacts with most and how to tailor communication to each stakeholder. When the user asks you to write something for a specific person, check this file first and adapt tone, detail level, and framing accordingly.

15. **`context/individual/my-writing-voice.md`**
    This person's voice rules layered on top of company brand voice. Words they use, words they avoid, sentence structure tendencies, and how their voice shifts by channel. Apply these rules to all individually-attributed output.

16. **`context/individual/my-goals-and-kpis.md`**
    What this person is measured on. When producing output, orient it toward these outcomes. A sales rep's outputs should lean toward pipeline impact. A marketer's should lean toward conversion. A finance person's should lean toward accuracy and compliance. Let this file subtly shape every output without being heavy-handed about it.

17. **`context/individual/my-meeting-cadence.md`**
    Recurring meetings, prep requirements, and follow-up expectations. When the user asks for meeting prep, check this file to understand what format and content is expected. When the user references a meeting by name, pull context from here.

18. **`context/individual/my-tools-and-logins.md`**
    Which tools this person uses and how they move between them. Produce output in the format that works with their tools. If they draft in Google Docs, don't produce Word files. If they share via Slack, format for easy pasting.

19. **`context/individual/my-frequently-asked.md`**
    Questions this person gets asked repeatedly and their approved answers. If the user's request matches a frequently asked question, use the approved language as a starting point and tailor to the specific context.

**After reading all 10 individual files:** You now have the full context stack. Company, department, and individual layers are loaded. Every output from this point forward should reflect all three layers.

---

### Step 4: Route to the Appropriate Skill File

Now that all context is loaded, determine what the user is asking for and check the `skills/` folder for a matching skill file.

**Routing logic:**

1. Parse the user's request to identify the task type (e.g., writing a blog post, preparing a proposal, building a financial model, drafting meeting notes)
2. Check `skills/` for a skill file that matches the task type
3. If a matching skill file exists, read it and execute the task following the skill file's instructions, combined with all the context loaded in Steps 1-3
4. If no matching skill file exists, execute the task using your best judgment informed by all the context loaded in Steps 1-3. After completing the task, suggest to the user that a skill file could be created for this task type to ensure consistency in the future.

**Priority rules when context conflicts:**

- Company glossary always applies (never override terminology)
- For company-attributed output (blog posts, marketing materials, press releases, case studies): company brand-voice.md takes precedence over individual voice files
- For individually-attributed output (emails, Slack messages, personal communications): individual communication-samples.md and my-writing-voice.md take precedence over company brand-voice.md
- Department workflows always apply unless the user explicitly asks to deviate
- Individual working-preferences.md overrides default Claude behavior in all cases (format preferences, communication style, guardrails)
- If a skill file contradicts a context file, the context file wins. Skill files define how to execute a task. Context files define the constraints within which all tasks are executed.

---

## Important Notes

**Do not narrate the loading process.** Do not tell the user "I'm now reading your company context files." Just read them and execute. The user should experience seamless, contextually-aware output from their first message.

**If a context file is missing or empty,** proceed with what's available. Do not halt or ask the user to create the missing file before continuing. Note the gap internally and work around it.

**If this is a new workspace with no context files yet,** inform the user that the workspace hasn't been configured with context files and direct them to the GitHub repo for the interview frameworks that will help them build out each file: [GITHUB REPO LINK]

**Update cadence reminders:**
- `active-projects.md` should be updated weekly
- Department and company context files should be reviewed quarterly
- Skill files should be refined whenever output quality drops or workflows change
- If you notice a context file appears outdated based on the user's current request, mention it after completing the task: "By the way, your active-projects.md still lists [project] as in progress. Want me to update it?"

## File Count

This orchestrator manages 19 sub-files across 3 context layers:
- 5 company context files
- 4 department context files
- 10 individual context files

Plus any number of skill files in the `skills/` folder, which grow over time as the team identifies new recurring tasks worth systematizing.

Total skill count including this orchestrator: **20 skills** (1 orchestrator + 19 context sub-skills).
