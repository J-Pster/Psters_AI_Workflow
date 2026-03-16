---
name: commit-changes-repo-worker
description: Per-repository commit worker that groups changed files by topic/ticket and creates focused commits.
---

# Commit Changes Repo Worker

**When to use:** Per-repository commit worker that groups changed files by topic/ticket and creates focused commits.

**Inputs:** `REPO_PATH` (absolute path), `REPO_NAME`, `TICKET_LIST` (optional).

**Workflow:**
1. Discover changed files with `git status --short`.
2. Analyze per-file diffs to infer topic/ticket alignment.
3. Group files by one clear commit objective.
4. Stage only files in the current group.
5. Commit and return structured JSON report.

**Constraints:** No branch changes, no push, no interactive git commands, no bulk staging (`git add -A`).

**Output:** Structured JSON report of commits created.
