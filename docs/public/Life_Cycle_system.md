# AI Application Development Lifecycle

This document outlines the full command progression for the automated
application development system. The workflow is divided into Planning,
Implementation, Validation, and Orchestration phases.

Commands orchestrate the workflow and update project state. Skills
perform the execution work.

------------------------------------------------------------------------

## 1. Planning Phase

### /brainstorm

Purpose: - Capture initial idea - Ask clarifying questions - Identify
assumptions

Output: docs/reference/brainstorm.md

------------------------------------------------------------------------

### /classify-app

Purpose: Identify application type (SaaS, AI tool, internal tool, mobile
app, etc.)

Output: docs/reference/app-classification.md

------------------------------------------------------------------------

### /generate-framework

Purpose: Define major modules and system boundaries.

Output: docs/reference/framework.md

------------------------------------------------------------------------

### /generate-prd

Purpose: Create detailed Product Requirements Document.

Output: docs/reference/prd.md

------------------------------------------------------------------------

### /stack-advisor

Purpose: Recommend technology stack.

Output: docs/reference/stack.md

------------------------------------------------------------------------

### /generate-architecture

Purpose: Define full system architecture.

Output: docs/reference/architecture-v1.md

------------------------------------------------------------------------

### /generate-plan

Purpose: Break architecture into executable tasks.

Output: docs/reference/plan.md

------------------------------------------------------------------------

## 2. Implementation Phase

### /scaffold-project

Create repository structure.

------------------------------------------------------------------------

### /build-database

Generate schema and migrations.

------------------------------------------------------------------------

### /build-backend

Implement backend services and API endpoints.

------------------------------------------------------------------------

### /extract-design-spec

Convert design exports into frontend architecture.

Output: docs/reference/frontend-architecture.md

------------------------------------------------------------------------

### /build-frontend

Generate UI components and pages.

------------------------------------------------------------------------

### /integrate-services

Connect frontend and backend services.

------------------------------------------------------------------------

### /write-tests

Generate automated tests.

Test structure: tests/unit tests/api tests/integration

------------------------------------------------------------------------

## 3. Validation Phase

### /run-tests

Execute test suite.

Output: validation-reports/test-results.json

------------------------------------------------------------------------

### /validate-architecture

Ensure code follows architecture rules.

Output: validation-reports/architecture-report.json

------------------------------------------------------------------------

### /drift-check

Detect divergence between specs and implementation.

Output: validation-reports/drift-report.json

------------------------------------------------------------------------

### /qa-review

Perform final quality review.

------------------------------------------------------------------------

### /auto-fix

Automatically repair detected issues.

------------------------------------------------------------------------

## 4. Orchestration Layer

### /project-engine

Coordinates the lifecycle and determines next step.

------------------------------------------------------------------------

### /advance-phase

Moves project to next lifecycle stage.

------------------------------------------------------------------------

### /status

Displays project health and current phase.

Reads: docs/reference/project-state.md validation-reports/

------------------------------------------------------------------------

## Lifecycle Overview

brainstorm → classify-app → generate-framework → generate-prd →
stack-advisor → generate-architecture → generate-plan → scaffold-project
→ build-database → build-backend → extract-design-spec → build-frontend
→ integrate-services → write-tests → run-tests → validate-architecture →
drift-check → qa-review → auto-fix

------------------------------------------------------------------------

## Core Principle

Commands = workflow orchestration Skills = execution modules
project-state = coordination layer validation-reports = feedback system
tests = verification layer
