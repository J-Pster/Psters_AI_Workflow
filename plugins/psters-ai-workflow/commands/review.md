---
name: review
description: Run a multi-angle review focused on regressions, risks, and simplification opportunities.
argument-hint: "[PR number, branch name, or path]"
---

# Review

**Objective:** Run a multi-angle review focused on regressions, risks, and simplification opportunities.

**Inputs:** PR number, branch name, or path.

**Steps:**
1. Determine review target (PR, branch, or local diff).
2. Gather changed files and diffs.
3. Run relevant review agents in parallel when available.
4. Prioritize findings by severity.
5. Output critical issues first, then recommendations.

**Output:** Findings ordered by severity; critical issues first, then recommendations.
