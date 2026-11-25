---
description: Simulate a Lean Portfolio Management review of one or more epic ideas
argument-hint: <epic idea(s)>
---

Create an **agent team** to take these idea(s) through the Portfolio Kanban: $ARGUMENTS

Spawn:
- `lpm` → `safe-portfolio-leadership`
- `epic-owner` → `safe-epic-owner`
- `ea` → `safe-enterprise-architect`
- `bo` → `safe-business-owner`

Tasks:
1. lpm: strategic themes, portfolio budget assumptions, guardrails, WIP limit on epics.
2. epic-owner: epic hypothesis statement + Lean Business Case + MVP per idea (depends on 1).
3. ea: technical feasibility, enabler epics needed, architecture risks (parallel with 2).
4. bo: expected business value and ROI view per epic (depends on 2).
5. epic-owner + ea + bo: challenge each other's assumptions via messages (debate, not consensus by default).
6. lpm: go / no-go per epic with rationale, updated Portfolio Kanban (depends on 3, 4, 5).

Synthesize: decision table, top risks, what the MVP must prove.
