# The Big Picture (simplified)

## Configurations
- **Essential SAFe** – the minimum: Agile teams on one Agile Release Train (ART).
- **Large Solution SAFe** – adds the Solution Train to coordinate several ARTs and suppliers.
- **Portfolio SAFe** – adds Lean Portfolio Management (strategy, funding, governance).
- **Full SAFe** – all of the above.

The official site now also presents **Core SAFe** (the classic operating model) alongside
**AI-Native SAFe** (an AI-oriented operating model introduced in 2026, with new elements such as
an *AI Value Architect* role and *PI Outcome Planning*). This library models **Core SAFe**;
see `sources.md` if you want to extend the team with AI-Native roles.

## Levels and roles

```
Portfolio        Portfolio Leadership (LPM/VMO) · Epic Owners · Enterprise Architect
                        │  epics, strategic themes, lean budgets
Large Solution   Solution Train Engineer · Solution Management · Solution Architect
                        │  capabilities, solution intent
ART              Business Owners · RTE · Product Management · System Architect · System Team
                        │  features, PI objectives
Team             Product Owner · Scrum Master/Team Coach · Agile Team members
                        │  stories, iterations
Foundation       SPCs / LACE · Lean-Agile leaders (span every level)
```

## The three "triads"
Each level has a content / technical / facilitation trio:

| Level | Content (what) | Technical (how) | Facilitation (flow) |
|---|---|---|---|
| Portfolio | Epic Owners + Portfolio Leadership | Enterprise Architect | VMO |
| Solution | Solution Management | Solution Architect | STE |
| ART | Product Management | System Architect | RTE |
| Team | Product Owner | Agile Team | SM/TC |

Use this table to route questions: *content* questions go to the content role, etc.

## Cadence
- **Iteration**: fixed timebox, usually 2 weeks.
- **Planning Interval (PI)**: typically 4 development iterations + 1 Innovation & Planning (IP) iteration (≈ 8–12 weeks).
- ARTs plan together at **PI Planning**, demo together at **System Demo**, and improve together at **Inspect & Adapt**.
