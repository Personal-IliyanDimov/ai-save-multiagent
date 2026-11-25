# Artifacts and work items

## Work item hierarchy
```
Epic (portfolio)  →  Capability (solution, optional)  →  Feature (ART, fits in a PI)  →  Story (team, fits in an iteration)
Enabler epic          Enabler capability                    Enabler feature                 Enabler story / Spike
```
Enablers extend the architectural runway or improve the development value stream
(exploration, architecture, infrastructure, compliance).

## Backlogs (all managed as Kanban systems)
| Backlog | Owner | Contains |
|---|---|---|
| Portfolio Backlog / Portfolio Kanban | Portfolio Leadership (+ Epic Owners) | Epics |
| Solution Train Backlog | Solution Management | Capabilities |
| ART Backlog | Product Management | Features |
| Team Backlog | Product Owner | Stories |

Portfolio Kanban states (simplified): Funnel → Reviewing → Analyzing (Lean Business Case) → Ready → Implementing (MVP, then persevere) → Done.

## Planning artifacts
- **Vision** and **Roadmap** (ART and Solution)
- **PI Objectives** — per team and per ART; *committed* vs. *uncommitted*; each has business value 1–10 from BOs
- **ART Planning Board** — features per team per iteration, dependencies (strings), milestones
- **ART PI Risks** — ROAM'd: Resolved, Owned, Accepted, Mitigated
- **Solution Intent** — current and intended behavior/design of the solution
- **NFRs** — system qualities that constrain backlogs
- **Architectural Runway** — existing code/infra that lets near-term features land without big redesign

## Economics
- **WSJF** = Cost of Delay / Job Duration (job size).
  Cost of Delay = User-Business Value + Time Criticality + Risk Reduction & Opportunity Enablement.
  Estimate each relatively with modified Fibonacci (1, 2, 3, 5, 8, 13, 20).
- **Capacity allocation**: % split of a PI between features, enablers, and maintenance/tech debt.
- **Lean budgets & guardrails**: fund value streams, not projects.

## Metrics (Measure and Grow)
- Flow: distribution, velocity, time, load, efficiency, predictability
- Outcomes: value stream KPIs, OKRs
- Competency: business agility self-assessments
- **ART predictability** = actual business value ÷ planned business value (target ~80–100%).
