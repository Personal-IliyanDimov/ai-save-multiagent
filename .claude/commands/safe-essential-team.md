---
description: Spawn the Essential SAFe role team (ART + one Agile team) for any task
argument-hint: <what the train should work on>
---

Create an **agent team** for this work: $ARGUMENTS

Spawn teammates from the SAFe agent types, named by role:
- `pm` (`safe-product-management`), `rte` (`safe-release-train-engineer`),
  `architect` (`safe-system-architect`), `po` (`safe-product-owner`),
  `sm` (`safe-scrum-master-team-coach`), `dev` (`safe-agile-team-developer`).
Use team name "alpha" for team-level roles.

Optional, only if the task needs them: `bo` (`safe-business-owner`), `systeam` (`safe-system-team`).

Rules for you as lead: decompose the work into tasks along SAFe flow (feature → story → build →
demo), respect file ownership in `CLAUDE.md`, let roles decide within their decision rights,
and wait for teammates before synthesizing.
