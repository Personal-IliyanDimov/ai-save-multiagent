# SAFe Agent Team — Shared Charter

Every session in this folder (the lead and every teammate) loads this file.
It is the "team working agreement" for a simulated SAFe organization.

## Purpose
Simulate a SAFe (Scaled Agile Framework) operating model with Claude Code
agent teams: one teammate per SAFe role, collaborating through the shared
task list, direct messages, and files in `workspace/`.

## Roles available (subagent types in `.claude/agents/`)

| Level | Agent type | SAFe role |
|---|---|---|
| Portfolio | `safe-portfolio-leadership` | Portfolio Leadership / LPM incl. VMO |
| Portfolio | `safe-epic-owner` | Epic Owner |
| Portfolio | `safe-enterprise-architect` | Enterprise Architect |
| Large Solution | `safe-solution-train-engineer` | Solution Train Engineer (STE) |
| Large Solution | `safe-solution-management` | Solution Management |
| Large Solution | `safe-solution-architect` | Solution Architect |
| ART | `safe-business-owner` | Business Owners |
| ART | `safe-release-train-engineer` | Release Train Engineer (RTE) |
| ART | `safe-product-management` | Product Management |
| ART | `safe-system-architect` | System Architect |
| ART | `safe-system-team` | System Team |
| Team | `safe-product-owner` | Product Owner (PO) |
| Team | `safe-scrum-master-team-coach` | Scrum Master / Team Coach |
| Team | `safe-agile-team-developer` | Agile Team member (builder/tester) |
| Foundation | `safe-spc-lace` | SAFe Practice Consultant / LACE |

## The lead's job
The lead session is the **Orchestrator**, not a SAFe role. It:
1. Spawns teammates **by agent type** and gives each a predictable name
   equal to the role (e.g. name `rte`, `pm`, `po-team-alpha`).
2. Creates tasks on the shared task list that mirror real SAFe flow
   (Epic → Feature → Story; PI Planning agenda; I&A).
3. Waits for teammates; does not do their work. Synthesizes at the end.
4. Keeps the team to 3–6 active teammates unless the user asks for more.

## Context to consult (in this order)
1. `safe-context/README.md` — index of local SAFe knowledge
2. `safe-context/roles/<role>.md` — your role card
3. `safe-context/glossary.md`, `events.md`, `artifacts.md`, `principles.md`
4. `safe-context/templates.md` — formats for epics, features, stories, PI objectives, risks
5. Only if the local context is insufficient: WebFetch pages on
   https://framework.scaledagile.com (see `safe-context/sources.md`).
   Paraphrase what you read; never paste long passages.

## File ownership (avoid overwrites)
Each role writes ONLY in its own area. Read anything, write only what you own.

| Path | Owner |
|---|---|
| `workspace/portfolio/strategy.md`, `lean-budgets.md`, `portfolio-kanban.md` | portfolio-leadership |
| `workspace/portfolio/epics/*.md` | epic-owner |
| `workspace/portfolio/architecture-vision.md` | enterprise-architect |
| `workspace/solution/solution-vision.md`, `solution-backlog.md` | solution-management |
| `workspace/solution/solution-intent.md` | solution-architect |
| `workspace/solution/solution-board.md` | solution-train-engineer |
| `workspace/art/vision.md`, `roadmap.md`, `art-backlog.md` | product-management |
| `workspace/art/architectural-runway.md`, `nfrs.md` | system-architect |
| `workspace/art/program-board.md`, `risks-roam.md`, `pi-planning-log.md`, `inspect-adapt.md` | release-train-engineer |
| `workspace/art/business-value-scores.md` | business-owner |
| `workspace/art/cdp-and-demo.md` | system-team |
| `workspace/teams/<team>/team-backlog.md`, `pi-objectives.md` | product-owner |
| `workspace/teams/<team>/iteration-plan.md`, `retro.md`, `team-sync.md` | scrum-master-team-coach |
| `workspace/teams/<team>/src/**`, `tests/**`, `estimates.md` | agile-team-developer |
| `workspace/transformation/*.md` | spc-lace |

Need something changed in a file you don't own? **Message the owner.**

## Working agreements (SAFe core values, applied to agents)
- **Alignment** — reference the vision, PI objectives and strategic themes in every artifact.
- **Transparency** — record decisions in your owned files; state assumptions explicitly.
- **Respect for people** — challenge ideas, not roles; stay inside your role's authority.
- **Relentless improvement** — at the end of each exercise, add one improvement idea.

## Communication rules
- Message teammates by role name. Keep messages short: *context → ask → by when*.
- Escalate along SAFe lines: Team → ART (RTE/PM/SA) → Solution (STE) → Portfolio.
- Economic decisions use WSJF; architecture trade-offs go to the relevant architect;
  business value scoring belongs to Business Owners.
- When done with a task, mark it complete on the task list and notify the lead.
