# Templates

## Epic hypothesis statement (Epic Owner)
```markdown
# EPIC-<id>: <name>   (Business | Enabler)
**For** <customers> **who** <need>, **the** <solution> **is a** <what>
**that** <benefit>. **Unlike** <competitor/current state>, **our solution** <differentiator>.

## Business outcomes (measurable)
- ...
## Leading indicators
- ...
## NFRs
- ...
## MVP
- Scope: ...   - Cost estimate: ...   - Hypothesis is proven when: ...
## Portfolio Kanban state: Funnel | Reviewing | Analyzing | Ready | Implementing | Done
## Decision log
```

## Feature (Product Management)
```markdown
### FEAT-<id>: <name>   (Business | Enabler)
- Benefit hypothesis: <we believe … will result in … measured by …>
- Acceptance criteria:
  - [ ] ...
- NFRs: ...
- Parent: EPIC-<id> / CAP-<id>
- WSJF: UBV <n> + TC <n> + RR/OE <n> = CoD <n> / Size <n> = **<wsjf>**
```

## Story (Product Owner)
```markdown
#### STORY-<id>: As a <persona>, I want <activity> so that <value>.
- Parent: FEAT-<id>    - Points: <1,2,3,5,8,13>
- Acceptance criteria (Given / When / Then):
  - Given ... When ... Then ...
```

## WSJF table
| Item | UBV | TC | RR/OE | CoD | Size | WSJF | Rank |
|---|---|---|---|---|---|---|---|

Score each column relatively: the smallest item gets 1 in each column, others relative to it.

## Capacity & load (SM/TC, per team)
| Iteration | Capacity (pts) | Load (pts) | Notes |
|---|---|---|---|
| I1 | | | |
| I2 | | | |
| I3 | | | |
| I4 | | | |
| IP | — | — | Innovation & Planning |
Capacity heuristic: 8 points per full-time builder/tester per 2-week iteration, minus 1 per day off.

## Team PI objectives (PO)
| # | Objective (SMART) | Committed? | Business value (BO, 1–10) | Actual value (I&A) |
|---|---|---|---|---|

## ART planning board (RTE)
| Team / Iteration | I1 | I2 | I3 | I4 | IP |
|---|---|---|---|---|---|
| Milestones | | | | | |
| Team A | FEAT-1 | | | | |
Dependencies: `Team A FEAT-1 (I2) ← needs ← Team B FEAT-3 (I1)`

## ROAM risk log (RTE)
| # | Risk | Raised by | Impact | ROAM | Owner | Action |
|---|---|---|---|---|---|---|

## I&A problem-solving workshop (RTE)
1. Problem statement (what, where, when, impact)
2. Root causes (fishbone categories: people, process, tools, program, environment)
3. 5 Whys on the biggest cause
4. Pareto vote → restated problem
5. Solutions brainstorm → improvement backlog items (owner, PI)
