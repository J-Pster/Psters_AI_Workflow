---
name: work-plan
description: Execute one phase from a plan file directly, then update status and docs.
argument-hint: "[path to plan file] [optional: phase]"
---

# Execute Plan Phase

**Objective:** Execute one phase from a plan file, then update status and docs.

**Inputs:** Path to plan file; optional phase.

**Steps:**
1. Read the target plan and supporting docs.
2. Select the requested or next pending phase.
3. Execute tasks in dependency order.
4. Run build/validation commands for changed areas.
5. Update plan checklist and phase status.
6. Summarize implementation and next step.

**Output:** Implementation summary and next step.
