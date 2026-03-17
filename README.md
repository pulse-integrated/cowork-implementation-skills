# Team Playbook Skills for Claude Cowork

A set of 20 skills that walk your team through building the context files Claude needs to actually be useful. Instead of staring at a blank markdown file and guessing what to write, each person gets an interview, answers questions conversationally (or drops in existing docs), and gets a finished context file out the other end.

Built by [Pulse](https://pulsemarketing.co).

## Pro Tip: Use Voice-to-Text to Move Even Faster

Each skill works by interviewing you, which means you're answering questions conversationally. Typing out those answers is the slowest part. Use [Wispr Flow](https://wisprflow.ai/r?SEAN813) to talk through your answers instead of typing them. Wispr Flow transcribes your speech directly into any text field on your computer, so you can speak naturally into the Cowork chat and your answers show up as text in real time. This cuts the time to complete all 20 skills roughly in half. Talk through your company overview in 5 minutes instead of typing it in 15.

## What This Is

When you deploy Claude Cowork across a team, output quality depends entirely on context. Generic prompts produce generic output. The fix is structured context files organized in three layers:

1. **Company Context** (5 files): built once by leadership, shared by everyone
2. **Department Context** (4 files): built by each department head, shared across the team
3. **Individual Context** (10 files): built by each person, unique to them

These 20 skills automate the creation of all 19 context files plus a master orchestrator that runs through the full sequence every session.

## How It Works

Install the skills into your Cowork workspace. The master skill (`team-playbook`) checks which files you've already built, shows your progress, and tells you what to work on next. Each sub-skill runs a guided interview, asks targeted questions, accepts uploaded materials (pitch decks, brand guides, wikis, whatever you've got), and outputs a clean markdown file to the right folder.

The whole thing follows a recommended sequence: company files first, then department, then individual. That order matters because each layer builds on the one before it.

## Prerequisites

Before installing these skills, you need:

- **Claude Desktop app** installed on your machine (macOS or Windows). Download at [claude.ai/download](https://claude.ai/download).
- **A paid Claude plan** (Pro, Max, Team, or Enterprise). Cowork is not available on free plans.
- **Code execution and file creation enabled** in Settings > Capabilities. Skills require the code execution environment to function.
- For **Team and Enterprise plans**: an Owner must enable Skills in Organization Settings > Skills before individual users can access them.

## Installation

There are three ways to install these skills depending on your setup. Pick the one that matches your situation.

### Option 1: Upload via Claude Desktop (Individual Users)

This is the simplest path for individual users on any paid plan.

1. Clone or download this repo to your computer.
2. Each skill lives in its own folder (e.g., `team-playbook/`, `build-company-overview/`, `build-brand-voice/`, etc.). Each folder contains a single `SKILL.md` file.
3. For each skill folder, create a ZIP file of the folder. The ZIP should contain the skill folder as its root, not as a subfolder. For example, zipping `build-company-overview/` should produce `build-company-overview.zip` with `SKILL.md` directly inside.
4. Open the Claude Desktop app.
5. Navigate to **Customize > Skills**.
6. Click **Upload** and select the ZIP file.
7. Repeat for each skill you want to install.
8. Verify each skill appears in your Skills list and is toggled on.

To install all 20 at once, you can zip each folder and upload them one by one. Start with `team-playbook` (the orchestrator), then the 5 company context skills, then the 4 department skills, then the 10 individual skills.

### Option 2: Admin Provisioning (Team and Enterprise Plans)

This is the recommended path for organizations rolling out to multiple users. The admin installs skills once, and they automatically appear for everyone.

1. Clone or download this repo.
2. ZIP each skill folder individually (same as Option 1).
3. Have an **Owner or Primary Owner** log into the Claude admin panel.
4. Navigate to **Organization Settings > Skills**.
5. Upload each skill ZIP file. Skills uploaded here are provisioned organization-wide and automatically appear for all users with a team indicator.
6. Individual users can then toggle each skill on or off in their own **Customize > Skills** menu, but they don't need to install anything themselves.

This is the path described in the playbook for the Week 1 admin setup. Build the skills once, push them to everyone.

### Option 3: Claude Code / Manual Placement

If you're using Claude Code or prefer to work directly with the file system:

1. Clone this repo.
2. Copy the skill folders to `~/.claude/skills/`. For example:
   ```
   cp -r team-playbook ~/.claude/skills/team-playbook
   cp -r build-company-overview ~/.claude/skills/build-company-overview
   ```
3. Each skill is immediately available. You can invoke them with `/skill-name` (e.g., `/team-playbook`) or Claude will load them automatically when your request matches the skill description.
4. Skills placed here are personal and work across all your projects.

### Quick Install Script (All 20 Skills to Claude Code)

If you want to install all 20 skills at once via the command line:

```bash
git clone [GITHUB REPO URL] team-playbook-skills
cd team-playbook-skills

# Copy all skill folders to Claude skills directory
for dir in */; do
  if [ -f "$dir/SKILL.md" ]; then
    cp -r "$dir" ~/.claude/skills/"$dir"
  fi
done

echo "Installed $(ls -d ~/.claude/skills/*/SKILL.md 2>/dev/null | wc -l) skills"
```

### Verifying Installation

After installing via any method:

1. Open Claude Desktop and switch to the **Cowork** tab.
2. Type `/team-playbook` or simply ask Claude: "What context files have I built so far?"
3. The orchestrator should activate, scan your workspace for existing context files, and show you a progress checklist.
4. If the skill doesn't trigger, check that it's toggled on in **Customize > Skills** and that **Code execution and file creation** is enabled in **Settings > Capabilities**.

## The Skills

### Master Orchestrator
| Skill | What It Does |
|-------|-------------|
| `team-playbook` | Progress tracker and router. Detects existing files, shows a checklist, guides users to the next skill in the sequence. Runs through all 19 sub-skills every session to load full context before executing any task. |

### Company Context (Layer 1, built by CEO/leadership)
| Skill | Output File | What It Captures |
|-------|-----------|-----------------|
| `build-company-overview` | `company-overview.md` | What the company does, who it serves, business model, differentiators |
| `build-brand-voice` | `brand-voice.md` | Tone, word choices, anti-patterns, real writing samples, voice by channel |
| `build-products-and-services` | `products-and-services.md` | Full offering catalog, pricing, objections, competitive positioning |
| `build-glossary` | `glossary.md` | Acronyms, jargon, codenames, client shorthand |
| `build-org-chart` | `org-chart.md` | Team structure, ownership map, communication preferences |

### Department Context (Layer 2, built by department heads)
| Skill | Output File | What It Captures |
|-------|-----------|-----------------|
| `build-department-overview` | `department-overview.md` | What the department does, key metrics, current priorities |
| `build-workflows` | `workflows.md` | SOPs, recurring processes, approval chains, handoff points |
| `build-templates` | `templates.md` | Standard formats, naming conventions, gold-standard examples |
| `build-tools-and-systems` | `tools-and-systems.md` | Software stack, data flows, integrations, access notes |

### Individual Context (Layer 3, built by each team member)
| Skill | Output File | What It Captures |
|-------|-----------|-----------------|
| `build-about-me` | `about-me.md` | Role, responsibilities, background, working style |
| `build-working-preferences` | `working-preferences.md` | Communication style, delegation preferences, pet peeves, hard boundaries |
| `build-active-projects` | `active-projects.md` | Current projects, statuses, deadlines, blockers (update weekly) |
| `build-communication-samples` | `communication-samples.md` | Real writing examples across channels, tone shifts by audience |
| `build-my-stakeholders` | `my-stakeholders.md` | Key people, their preferences, how to tailor communication to each |
| `build-my-writing-voice` | `my-writing-voice.md` | Personal writing rules, word choices, sentence patterns, style influences |
| `build-my-goals-and-kpis` | `my-goals-and-kpis.md` | What you're measured on, targets, tracking status |
| `build-my-meeting-cadence` | `my-meeting-cadence.md` | Recurring meetings, prep needed, follow-up produced |
| `build-my-tools-and-logins` | `my-tools-and-logins.md` | Personal tool workflow, drafting vs. finalizing locations, output format preferences |
| `build-my-frequently-asked` | `my-frequently-asked.md` | Repeat questions and standard answers, with audience variations |

## Output Folder Structure

All files save to this structure in the user's workspace:

```
team-playbook/
└── SKILL.md                    ← the orchestrator
context/
├── company/
│   ├── company-overview.md
│   ├── brand-voice.md
│   ├── products-and-services.md
│   ├── glossary.md
│   └── org-chart.md
├── department/
│   ├── department-overview.md
│   ├── workflows.md
│   ├── templates.md
│   └── tools-and-systems.md
└── individual/
    ├── about-me.md
    ├── working-preferences.md
    ├── active-projects.md
    ├── communication-samples.md
    ├── my-stakeholders.md
    ├── my-writing-voice.md
    ├── my-goals-and-kpis.md
    ├── my-meeting-cadence.md
    ├── my-tools-and-logins.md
    └── my-frequently-asked.md
```

## Recommended Rollout Sequence

**Week 1:** CEO or senior leader builds all 5 company context files (30-45 minutes total).

**Week 1-2:** Each department head builds 4 department context files (15-30 minutes per department).

**Week 2-3:** Individual team members build their 10 personal context files. The first 3 (about-me, working-preferences, active-projects) take about 10 minutes. The remaining 7 take another 15-20 minutes but pay for themselves immediately.

For a detailed week-by-week rollout plan with specific owners, deliverables, and measurement frameworks, see the full [Cowork Team Deployment Playbook](link-to-playbook).

## Troubleshooting

**Skills aren't showing up in Cowork:**
- Confirm Code execution and file creation is enabled in Settings > Capabilities.
- For Team/Enterprise users: confirm your Owner has enabled Skills in Organization Settings > Skills.
- Verify the skill is toggled on in Customize > Skills.

**Claude isn't triggering a skill automatically:**
- Try invoking it directly with `/skill-name` (e.g., `/build-brand-voice`).
- Be more explicit in your request: "Use the build-brand-voice skill to help me create my brand voice file."
- Check that the skill's SKILL.md file has a clear description in the frontmatter.

**Skills appear greyed out:**
- Code execution may be disabled at the organization level (Team/Enterprise). Check with your Owner.

**ZIP upload fails:**
- Make sure the ZIP contains the skill folder as its root. If you see `folder/folder/SKILL.md` when you unzip, you've nested one level too deep. The ZIP should unpack to `folder/SKILL.md`.

## Time Investment

- Company context: ~45 minutes (one-time, by leadership)
- Department context: ~20 minutes per department (one-time, by department head)
- Individual context: ~30 minutes per person (one-time, with weekly updates to active-projects)

Total for a 50-person company with 5 departments: roughly 4-5 hours of interview time across all participants, spread over 2-3 weeks. The alternative is every person on the team starting from scratch every time they open Cowork.