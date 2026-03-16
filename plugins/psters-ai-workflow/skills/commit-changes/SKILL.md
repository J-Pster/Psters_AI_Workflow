---
name: commit-changes
description: Commit uncommitted changes with focused grouping, ticket-aware messages, and parallel per-repo workers when needed.
---

# Commit Changes

**When to use:** User asks to commit current work, with or without ticket IDs.

**Workflow:**
1. Parse ticket IDs/context from user input when provided.
2. Discover repositories with uncommitted changes.
3. Spawn one worker per repo in parallel using `skills/commit-changes-repo-worker/SKILL.md`.
4. Summarize generated commits and failures.

Follow the full workflow in `commands/commit-changes.md`.

**Constraints:** No branch changes or push unless explicitly requested. Stage precise file groups; avoid bulk staging.

**Output:** Summary of generated commits and any failures.
