---
name: write-tests
description: Generate automated tests for backend services, APIs, and application workflows.
---

# Write Tests

Generate automated tests that verify system functionality.

---

# Inputs

Read the following reference files:

- docs/reference/prd.md
- docs/reference/architecture.md
- docs/reference/plan.md

Use these to determine required test coverage.

---

# Test Categories

## 1. Unit Tests

Test individual services and business logic.

Examples:

services/projectService.ts  
services/userService.ts

Output:

tests/unit/projectService.test.ts

---

## 2. API Tests

Verify backend endpoints.

Examples:

GET /projects  
POST /projects

Output:

tests/api/projects.test.ts

---

## 3. Integration Tests

Test full workflows across layers.

Example workflow:

create project  
add task  
retrieve tasks

Output:

tests/integration/projectWorkflow.test.ts

---

# Supporting Files

Generate supporting utilities if needed:

tests/mocks/  
tests/utils/

Examples:

mockAuth.ts  
createTestUser.ts

---

# Test Directory Structure

Ensure the following structure exists:

tests/

tests/unit  
tests/api  
tests/integration  
tests/mocks  
tests/utils  

---

# Output

Generated test files for the application.
