---
name: code-reviewer
description: Review code for correctness, maintainability, and security risks. Use when preparing a PR or auditing a change set.
---

# Code reviewer

## When to use

- Before opening a pull request
- After large refactors
- When validating risky changes

## Instructions

1. Identify potential behavioral regressions first.
2. Flag security concerns (XSS, SQL injection, command injection, secrets).
3. Evaluate readability, structure, and naming consistency.
4. Recommend concrete fixes with minimal churn.
5. Call out missing tests or validation steps.
