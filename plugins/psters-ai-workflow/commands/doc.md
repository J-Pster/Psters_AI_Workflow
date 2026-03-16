---
name: doc
description: Generate or refresh technical documentation for modules, features, architecture, and decisions.
argument-hint: "module <name> | feature <name> | architecture | update | adr <decision>"
---

# Documentation

**Objective:** Generate or refresh technical documentation for modules, features, architecture, and decisions.

**Inputs:** Target and mode (e.g. `module <name>`, `feature <name>`, `architecture`, `update`, `adr <decision>`).

**Steps:**
1. Parse the documentation target and mode.
2. Read current code and existing docs for that scope.
3. Update or generate the requested documentation.
4. Remove stale references and contradictions.
5. Report what was documented and where.

**Output:** Summary of what was documented and file locations.
