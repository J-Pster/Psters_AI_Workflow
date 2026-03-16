---
name: deploy-lambda
description: Deploy one Lambda or all Lambdas in the current repository using project deployment scripts.
argument-hint: "[lambda-name or 'all']"
---

# Deploy Lambda

**Objective:** Deploy one Lambda or all Lambdas in the current repository using project deployment scripts.

**Inputs:** Lambda name or `all` (from argument-hint).

**Steps:**
1. Confirm current repository is the correct Lambda repo.
2. Verify deployment scripts available in `scripts/`.
3. Deploy one function or all functions based on argument.
4. Report success/failure with next action when needed.

**Output:** Deployment result and actionable next steps on failure.
