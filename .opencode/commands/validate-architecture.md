---
description: Validate that the codebase follows the defined system architecture.
agent: plan
subtask: true
---

Use the `validate-architecture` skill.

Inputs:
- docs/reference/architecture.md
- repository structure

Checks:
- folder structure matches architecture.md
- layer boundaries are respected
- dependency directions are correct

Output:
Report any violations or confirm architecture compliance.
