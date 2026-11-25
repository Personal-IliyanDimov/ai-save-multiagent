# safe-folder — a SAFe role team for Claude Code agent teams

One Claude Code agent per SAFe role (15 roles), a shared team charter, a local SAFe
knowledge library, and ready-made kickoff commands for common SAFe events.

## Requirements
- Claude Code **v2.1.32 or later** (`claude --version`)
- Agent teams are **experimental**; this folder enables them via `.claude/settings.json`
  (`CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS=1`). You can also export the variable in your shell.
- Optional: tmux or iTerm2 for split panes (`"teammateMode": "auto"` or `"tmux"`).

## Quick start
```bash
cd safe-folder
claude               # trust the folder when asked, so the agent definitions load
```
Then in Claude Code:
```
/safe-pi-planning A mobile app that lets Zurich commuters pool e-bike rentals
```
Navigate teammates with ↑/↓ in the agent panel, Enter to open one and talk to it directly,
Ctrl+T to toggle the shared task list.

Prefer free-form? Just ask:
```
Create an agent team. Spawn a teammate using the safe-release-train-engineer agent type named rte,
and one using safe-product-management named pm, to prepare PI Planning for <your product>.
```

## What's inside
```
safe-folder/
├── CLAUDE.md                     # team charter: roles, lead behavior, file ownership, comms rules
├── .claude/
│   ├── settings.json             # enables agent teams, pre-approves workspace edits + SAFe site fetches
│   ├── agents/                   # 15 subagent definitions = SAFe roles (usable as teammates)
│   │   ├── safe-portfolio-leadership.md   safe-epic-owner.md   safe-enterprise-architect.md
│   │   ├── safe-solution-train-engineer.md safe-solution-management.md safe-solution-architect.md
│   │   ├── safe-business-owner.md  safe-release-train-engineer.md  safe-product-management.md
│   │   ├── safe-system-architect.md  safe-system-team.md
│   │   ├── safe-product-owner.md  safe-scrum-master-team-coach.md  safe-agile-team-developer.md
│   │   └── safe-spc-lace.md
│   └── commands/                 # kickoff scenarios
│       ├── safe-pi-planning.md        # 5 teammates, full PI Planning flow
│       ├── safe-essential-team.md     # generic ART + team for any task
│       ├── safe-portfolio-review.md   # epics through the Portfolio Kanban
│       ├── safe-large-solution.md     # Solution Train Pre-Plan
│       ├── safe-inspect-adapt.md      # I&A on the current workspace
│       └── safe-refresh-context.md    # re-pull context from framework.scaledagile.com
├── safe-context/                 # local, paraphrased SAFe knowledge (read before the web)
│   ├── README.md  big-picture.md  events.md  artifacts.md  principles.md
│   ├── glossary.md  templates.md  sources.md
│   └── roles/<role>.md           # one role card per agent
└── workspace/                    # where the team writes artifacts (ownership in CLAUDE.md)
    ├── portfolio/  solution/  art/  teams/<team>/  transformation/
```

## How it works
- Each file in `.claude/agents/` is a **subagent definition**. When you ask the lead to spawn a
  teammate *using that agent type*, Claude Code applies the definition's `tools`, `model`, and
  body (role instructions) to the teammate.
- Every teammate loads `CLAUDE.md` automatically, so they share the charter, ownership map, and
  communication rules — but **not** the lead's conversation, which is why the commands put product
  context into each spawn prompt.
- Coordination happens through the shared task list (with dependencies) and direct messages.
- Each role writes only its own files in `workspace/` to avoid overwrites.

## Tips
- **Start small.** 3–6 teammates is the sweet spot; token use grows linearly per teammate.
  Don't spawn all 15 at once — pick the roles the scenario needs.
- If Claude uses plain subagents instead of a team, say "create an **agent team**".
- If the lead starts doing roles' work itself: "Wait for your teammates to finish."
- Teammates in in-process mode are not restored by `/resume`; ask the lead to respawn them.
- Want cheaper runs? Change `model: inherit` to `model: sonnet` or `haiku` in selected agent files.
- Agents also work as **ordinary subagents** with agent teams turned off — e.g.
  "use the safe-product-owner subagent to write stories for FEAT-3".

## Extending
- Add a role: copy any agent file, change `name`, `description`, ownership, and add a role card.
- AI-Native SAFe (added to the SAFe site in 2026) introduces roles like an AI Value Architect —
  run `/safe-refresh-context AI-Native SAFe` and create a new agent from the result.

## Disclaimer
The context library is a simplified paraphrase for experimentation, not official guidance.
SAFe® and Scaled Agile Framework® are registered trademarks of Scaled Agile, Inc.
Authoritative source: https://framework.scaledagile.com
