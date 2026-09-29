---
name: baby-fever-triage
description: 2 AM fever decision support — age triage, red flags, weight-based dosing that refuses to guess.
version: 1.0.0
author: Denis Voronin
license: MIT
tags: [fever, triage, dosing, parenting, infant-health]
---

# Baby Fever Triage

**One question at 2 AM: ER now, doctor today, or home care?**

Age-aware verdicts (under 3 months = automatic urgent), a 14-item red-flag
checklist where any YES means emergency, weight-based acetaminophen/ibuprofen
dosing that **refuses to state mL until you read the actual bottle
concentration**, an interval-verified alternating-dose scheduler, an illness
log, and a one-page pediatrician handoff summary.

## Quick Start
```bash
python3 scripts/fever.py triage --age-months 7 --temp 39.1 --unit c
python3 scripts/fever.py flags
python3 scripts/fever.py dose --drug acetaminophen --weight-kg 8.2 --conc mg-per-ml:100
python3 scripts/fever.py schedule --weight-kg 8.2 --hours 12
python3 scripts/fever.py handoff
```

100% local, one JSON file. Informational support — not a doctor; parental
instinct outranks this tool.
