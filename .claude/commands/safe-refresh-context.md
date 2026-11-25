---
description: Refresh the local SAFe context library from framework.scaledagile.com
argument-hint: [optional role or topic to refresh]
allowed-tools: WebFetch, Read, Write, Edit
---

Refresh `safe-context/` from the public SAFe site. Topic filter (optional): $ARGUMENTS

1. Read `safe-context/sources.md` for entry points.
2. WebFetch the glossary and the relevant role/event articles (only framework.scaledagile.com).
3. Update the matching files in `safe-context/` (role cards, glossary, events, artifacts).
4. Rules: **paraphrase in your own words**, keep each role card under ~60 lines, no long verbatim
   quotes, add the source URL at the bottom of each updated file, and update the
   "Snapshot taken" date in `safe-context/README.md`.
5. Report what changed (one line per file).
