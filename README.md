# Mina's Convene Startup OS

Your AI system for building Convene — the all-in-one conference operations platform for student clubs. Three agents that handle customer discovery, competitive intelligence, and product design so you can focus on talking to organizers and making decisions.

## What's Inside

| Agent | What It Does |
|-------|-------------|
| **@conference-detective** | Analyzes survey results, tracks hypotheses, designs experiments, manages discovery conversations. Your customer research engine. |
| **@platform-scout** | Maps every competitor and tool in the space. Builds feature gap matrices. Finds where Convene wins. |
| **@blueprint-builder** | Translates research into product: conference templates, onboarding flows, feature priorities, and business models. |

## Setup (One-Time, ~10 Minutes)

### 1. Install Claude Code

Download from [claude.ai/code](https://claude.ai/code) (Mac, Windows, or CLI).

### 2. Clone This Repo

```bash
git clone https://github.com/polarbaker/mina-convene-os.git
cd mina-convene-os
```

### 3. Set Up Google Workspace Connection

This OS uses Google Docs, Sheets, Slides, Calendar, and Gmail. Connect your Google account once:

```bash
npx -y google-workspace-mcp serve
```

Follow the prompts to authorize. The credential stays on your machine.

### 4. Open Claude Code in This Directory

```bash
claude
```

Or open the Claude Code desktop app and point it to this folder.

### 5. Try It

```
@conference-detective analyze the survey results
```

```
@platform-scout how is Convene different from Eventbrite?
```

```
@blueprint-builder design the onboarding flow for a new club
```

## File Structure

```
mina-convene-os/
├── CLAUDE.md                                  # System instructions (agents read this)
├── .mcp.json                                  # Tool connections (Google Workspace)
├── README.md                                  # This file (setup guide for you)
└── .claude/
    └── skills/
        ├── conference-detective/SKILL.md      # How @conference-detective works
        ├── platform-scout/SKILL.md            # How @platform-scout works
        └── blueprint-builder/SKILL.md         # How @blueprint-builder works
```

## How It Works (Non-Technical)

When you open Claude Code in this folder, it reads `CLAUDE.md` and understands it's your Convene startup OS with three specialized agents. Each agent has a skill file describing what it does, what steps it follows, and what it produces.

The `.mcp.json` file connects Claude Code to your Google Workspace — so agents can read and write Docs, Sheets, Slides, Calendar, and Gmail.

Talk to the system in plain English. Mention an agent name to activate its specialty. The agents work together: what @conference-detective learns feeds @platform-scout's analysis, which feeds @blueprint-builder's designs.

## Key Links

- **Survey (questions):** https://docs.google.com/forms/d/1wQmEDYQqEDU7Px1iDxokLA03hxBKKWg5VwdesS_QCZM/viewform
- **Survey (results):** https://docs.google.com/forms/d/1wQmEDYQqEDU7Px1iDxokLA03hxBKKWg5VwdesS_QCZM/edit
- **Wireframe:** (link TBD)

## Privacy

- Everything runs locally on your machine
- Google Workspace data stays in your Google account
- No student or attendee PII is processed by the system

## Questions?

This OS was built as part of HBS Strategy for Entrepreneurs (1257). For questions about the system design or customization, reach out to Gold Star AI.
