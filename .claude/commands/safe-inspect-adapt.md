---
description: Run an Inspect & Adapt event on the current workspace
---

Create an **agent team** to run Inspect & Adapt on the artifacts in `workspace/`.

Spawn: `rte` (`safe-release-train-engineer`), `pm` (`safe-product-management`),
`bo` (`safe-business-owner`), `sm` (`safe-scrum-master-team-coach`), `spc` (`safe-spc-lace`).

1. bo: score actual vs. planned business value per PI objective → ART predictability.
2. pm + sm: qualitative review — what worked, what did not.
3. rte: problem-solving workshop (template in `safe-context/templates.md`) on the top problem.
4. spc: SAFe fidelity review of the whole simulation and coaching recommendations.
Output: `workspace/art/inspect-adapt.md` (rte) and `workspace/transformation/fidelity-review.md` (spc).
