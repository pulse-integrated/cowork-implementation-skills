---
name: build-my-meeting-cadence
description: Build the my-meeting-cadence.md individual context file through a guided interview. Maps recurring meetings, what prep each needs, and what follow-up each produces. Turns meeting prep from a scramble into a system. Use this skill when someone says "build my meeting cadence," "my meetings file," "recurring meetings," "meeting prep," "calendar context for claude," or "help me prep for meetings." Part of the Team Playbook system (Layer 3, File 8 of 10).
---

# Build My Meeting Cadence

You are having a conversation with an individual to build their `my-meeting-cadence.md` file. This file maps their recurring meetings so Claude knows what each meeting is, who's in it, and what format the prep should take. When someone says "prep me for my Monday pipeline review," Claude already knows what that meeting is and what's needed.

Your tone should be organized and practical. You're building a system that eliminates the weekly scramble of meeting prep.

## Before Starting the Interview

Ask: **"Can you share your calendar or just list out your recurring meetings? I need the meeting name, who's in it, and how often it happens. If you can paste from your calendar app, great. Otherwise just list them."**

## Interview Flow

### Section 1: Meeting Inventory
- "Let's list all your recurring meetings. Weekly, biweekly, monthly, quarterly, all of them."
- For each: "What's the meeting called, how often, and who's in it?"

### Section 2: Meeting Details
For each recurring meeting:
- "What's the actual purpose of this meeting? Not the calendar description, the real reason it exists."
- "Do you lead this meeting or attend it? That changes what prep looks like."
- "What prep does this meeting need? Data pulls, status updates, talking points, a read-ahead doc?"
- "What typically comes out of this meeting? Action items, summary emails, updated trackers?"

### Section 3: Meeting Prep Patterns
- "Are there meetings where you consistently scramble to prepare? The ones where you're pulling things together 10 minutes before?"
- "Which meetings could Claude help you prep for most effectively?"

### Section 4: Focus Time
- "Are there time blocks or days where you protect focus time? Times Claude should know you're not in meetings and are doing deep work?"
- "Any calendar patterns Claude should be aware of? Like 'Monday mornings are always meetings' or 'Friday afternoons are wrap-up time.'"

## After the Interview

### Output Format

```markdown
# My Meeting Cadence

## Recurring Meetings

### [Meeting Name]
**Frequency:** [Weekly/Biweekly/Monthly/Quarterly]
**Day/Time:** [When it happens]
**Duration:** [Length]
**Attendees:** [Who's in the room]
**My Role:** [Lead/Participant/Presenter]
**Purpose:** [The real reason this meeting exists]
**Prep Needed:**
- [What to prepare, in what format]
**Follow-Up Produced:**
- [What comes out of this meeting]
**Claude Can Help With:** [Specific ways Claude can assist with prep or follow-up]

---

### [Meeting Name 2]
[Same format]

---

## Focus Time / Protected Blocks
| Day/Time | Purpose | Notes |
|----------|---------|-------|
| [Block] | [What it's for] | [Any rules] |

## Meeting Prep Priority
[Ranked list of meetings where Claude's help would save the most time]
1. [Meeting] - [Why Claude can help most here]
2. [Meeting] - [Why]
3. [Meeting] - [Why]
```

### Writing Rules
- First person
- Be specific about prep requirements. "Prepare for the meeting" is useless. "Pull this week's pipeline numbers from the CRM, compare to last week, and write 3 talking points about deals at risk" is what Claude needs.
- Include the actual day/time so Claude can be contextually aware
- The "Claude Can Help With" line is the most actionable part, make it specific

## Saving the File

Save to `context/individual/my-meeting-cadence.md`.

After saving: "Meeting cadence is mapped. Next is my-tools-and-logins.md, where we capture your personal tool workflow. Say **'build my tools and logins'** when you're ready."
