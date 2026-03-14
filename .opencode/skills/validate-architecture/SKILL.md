---
name: validate-architecture
description: Validate that the generated codebase follows the system architecture specification.
---

# Validate Architecture

Ensure the repository structure and dependencies follow the rules defined in the architecture specification.

---

# Inputs

Read the following reference files:

- docs/reference/architecture.md
- docs/rules/architecture-rules.md (if present)

Scan the entire repository structure.

---

# Validation Categories

## 1. Folder Structure

Verify that files exist in the directories defined by the architecture.

Example expected structure:

api/
services/
repositories/
db/
components/
hooks/
layouts/
tests/

Example violations:

- file located in incorrect folder
- missing required directory
- duplicate module structure

---

## 2. Layer Boundaries

Ensure correct dependency flow.

Valid architecture pattern:

Controller  
↓  
Service  
↓  
Repository  
↓  
Database

Violations:

- controllers accessing database directly
- services importing UI components
- repositories importing controllers

---

## 3. Frontend / Backend Separation

Ensure frontend and backend code remain isolated.

Violations:

- frontend components importing backend services
- backend code importing UI modules

---

## 4. Dependency Direction

Ensure dependencies flow only downward.

Valid:

controllers → services → repositories

Invalid:

repositories importing controllers

---

## 5. File Placement

Ensure files follow expected conventions.

Examples:

controllers inside `/api`
services inside `/services`
database models inside `/db`

---

# Generate Validation Report

Write the results to:

reports/validation-reports/architecture-report.json

Example structure:

{
  "status": "fail",
  "violations": [
    {
      "type": "layer_violation",
      "file": "controllers/projectController.ts",
      "issue": "Controller accessing database directly"
    },
    {
      "type": "structure_violation",
      "file": "services/auth.ts",
      "issue": "File located in incorrect directory"
    }
  ]
}

---

# Output

If no violations exist:

Architecture validation passed.

If violations exist:

Architecture violations detected.
