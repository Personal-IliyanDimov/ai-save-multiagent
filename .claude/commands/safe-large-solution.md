---
description: Simulate Solution Train Pre-Plan across multiple ARTs
argument-hint: <large solution description>
---

Create an **agent team** to simulate a Solution Train Pre-Plan for: $ARGUMENTS

Spawn:
- `ste` → `safe-solution-train-engineer`
- `sol-mgmt` → `safe-solution-management`
- `sol-arch` → `safe-solution-architect`
- `rte-a` → `safe-release-train-engineer` (ART "A", files under `workspace/art/`)
- `pm-a` → `safe-product-management` (ART "A")

Assume a second ART "B" and one supplier exist; the lead role-plays them only when asked.

Tasks: solution vision & capabilities with WSJF (sol-mgmt) → solution intent, integration points,
NFRs (sol-arch) → split capabilities into ART-A features (pm-a) → cross-ART dependency and risk map
(ste + rte-a) → Pre-Plan readout (ste).
