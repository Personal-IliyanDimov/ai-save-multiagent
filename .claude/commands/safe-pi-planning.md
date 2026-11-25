---
description: Run a simulated SAFe PI Planning with an agent team (Essential SAFe ART)
argument-hint: <product idea or path to a brief>
---

Create an **agent team** (not plain subagents) to simulate PI Planning for one Agile Release Train.

Product / context: $ARGUMENTS

Spawn these teammates using the named agent types, with exactly these names:
- `pm` → agent type `safe-product-management`
- `rte` → agent type `safe-release-train-engineer`
- `architect` → agent type `safe-system-architect`
- `po-alpha` → agent type `safe-product-owner` (team "alpha", files under `workspace/teams/alpha/`)
- `dev-alpha` → agent type `safe-agile-team-developer` (team "alpha")

Give each teammate in its spawn prompt: the product context above, its team name if any, and the instruction to read `CLAUDE.md` and its role card first.

Create shared tasks that follow `safe-context/events.md` → PI Planning, with dependencies:
1. pm: vision + top 5–8 features with WSJF → `workspace/art/`
2. architect: architecture vision, NFRs, enabler features (can run in parallel with 1)
3. rte: PI Planning agenda + empty planning board + ROAM log (parallel with 1–2)
4. po-alpha: split features into stories with acceptance criteria (depends on 1)
5. dev-alpha: estimate stories, capacity/load for 4 iterations, raise risks (depends on 4)
6. po-alpha: draft team PI objectives, committed/uncommitted (depends on 5)
7. rte: draft plan review — planning board, dependencies, ROAM all risks (depends on 2, 6)
8. pm + architect: management review — adjust scope if overloaded (depends on 7)
9. rte: final plan + simulated confidence vote from each teammate, with reasons (depends on 8)

You (lead) play the Business Owners unless the user asks to add a `safe-business-owner` teammate:
assign business value 1–10 to each team PI objective after task 6.

Wait for teammates to complete their tasks before synthesizing. Finish with a summary:
PI objectives with business value, planning board, top ROAM'd risks, confidence vote, and one
improvement per role.
