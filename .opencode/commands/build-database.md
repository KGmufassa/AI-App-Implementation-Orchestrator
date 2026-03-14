---
description: Generate database schema and migrations from the architecture data model
agent: build
subtask: true
---

# Build Database Command

Use the `build-database` skill to generate the database layer for the project.

The database must be built using the architecture artifacts produced during the planning phase.

Required context:

- docs/reference/architecture.md
- docs/reference/stack.md
- docs/reference/plan.md

Invoke the `build-database` skill.

Ensure the following artifacts are created:

- database schema
- migrations
- models or ORM mappings
- indexes and constraints

Validate that:

- all entities defined in the architecture exist
- relationships are correctly implemented
- migrations can run successfully

Output only the confirmation message:

"Database schema and migrations successfully generated."

---

# Update Project State

Update the following file:

docs/reference/project-state.md

Modify:

Phase: [CURRENT_COMMAND_PHASE]
Last Updated: [CURRENT_TIMESTAMP]

Save changes.
