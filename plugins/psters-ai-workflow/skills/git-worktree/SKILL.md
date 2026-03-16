---
name: git-worktree
description: Manages Git worktrees for isolated parallel development. Use when creating separate working directories for branches without switching the main repo.
---

# Git Worktree

**When to use:** Creating isolated working directories for parallel branch work without switching the main repo.

**Workflow:**
- List: `git worktree list`
- Add: `git worktree add <path> <branch>` (e.g. `git worktree add ../my-feat ../feature-branch`)
- Remove: `git worktree remove <path>` (after switching away and committing or discarding)

**Constraints:** Run commands from repo root. For multi-repo workspaces, create worktrees from the repo that contains the target branch.

**Output:** Worktree path and branch ready for isolated work.
