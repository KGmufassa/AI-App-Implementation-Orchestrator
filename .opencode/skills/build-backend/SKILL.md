---
name: build-backend
description: Generate backend services, repositories, controllers, and middleware using the architecture and database schema.
---

# Build Backend Skill

This skill generates the server-side logic of the application.

It creates controllers, services, and repository layers that interact with the database models.

---

# Required Inputs

- docs/reference/architecture.md
- docs/reference/prd.md
- docs/reference/plan.md
- db/schema
- db/models

If any artifacts are missing, stop execution.

---

# Step 1: Identify Backend Framework

Read stack.md to determine backend framework.

Examples:

FastAPI
Node Express
NestJS
Django
Spring Boot

---

# Step 2: Identify Application Entities

From database models identify entities such as:

User
Project
Task
Session

Each entity should map to:

- controller
- service
- repository

---

# Step 3: Generate Repository Layer

Repositories provide database access.

Create:

/services/repositories

Example:

/services/repositories/userRepository.ts

Repository responsibilities:

- create
- read
- update
- delete
- query filtering

---

# Step 4: Generate Service Layer

Services contain business logic.

Create:

/services

Example:

/services/userService.ts

Service responsibilities:

- validation rules
- authorization checks
- business workflows
- interaction with repositories

---

# Step 5: Generate Controllers / Routes

Controllers expose API endpoints.

Create:

/api

Example endpoints:

GET /users
POST /users
GET /projects
POST /tasks

Controllers must:

- call services
- validate requests
- return structured responses

---

# Step 6: Add Validation Schemas

Create request validation using framework conventions.

Example:

/api/validators

Use libraries defined in stack.md such as:

zod
pydantic
class-validator

---

# Step 7: Add Middleware

Create middleware for:

authentication  
authorization  
logging  
error handling  

Example:

/middleware/auth
/middleware/errorHandler

---

# Step 8: Wire Dependencies

Connect controllers → services → repositories → models.

Ensure imports are correct.

---

# Step 9: Validation

Verify:

- API endpoints exist for all entities
- services call repositories
- repositories use models
- request validation exists
- middleware registered

If any layer is missing, halt execution.

---

# Output

After execution the repository must contain:

/api
/services
/services/repositories
/api/validators
/middleware
