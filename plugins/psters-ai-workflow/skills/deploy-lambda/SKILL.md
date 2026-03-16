---
name: deploy-lambda
description: Deploy Lambda functions using repository deployment scripts from the Lambda repo root.
---

# Deploy Lambda

**When to use:** Deploying Lambda functions using repository deployment scripts.

**Workflow:**
1. Confirm you are in the correct Lambda repository root.
2. Locate deployment scripts in `scripts/` (single-function and/or all-functions).
3. Run deployment for one function or all functions based on request.
4. Report deployment outcome and actionable failure hints.

**Constraints:** Use repository scripts only; no ad-hoc manual packaging. Use explicit profile/region flags when scripts support them. Validate function names with script help output when unsure.

**Output:** Deployment outcome and actionable failure hints.
