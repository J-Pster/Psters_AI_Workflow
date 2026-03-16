---
name: commit-changes
description: Create focused commits from current changes, grouping by topic or ticket when provided.
argument-hint: "[optional ticket IDs or context]"
---

# Commit Changes

**Objective:** Create focused commits from current changes, grouping by topic or ticket when provided.

**Inputs:** Optional ticket IDs or context (from argument-hint).

**Steps:**
1. Discover all changed files in the active repository.
2. Group files by one clear topic (or ticket) per commit.
3. Stage only files for the current commit group.
4. Commit using conventions from `rules/commits.mdc`.
5. Summarize generated commit messages and remaining changes.

**Output:** Summary of commits created and any remaining changes.
