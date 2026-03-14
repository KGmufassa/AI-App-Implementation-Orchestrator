---
name: build-frontend
description: Generate UI code using the frontend architecture and backend endpoints.
---

# Build Frontend

Convert the UI architecture specification into working frontend code.

---

## Inputs

- docs/reference/frontend-architecture.md
- design/
- api/

---

## Step 1 — Read UI Architecture

Parse:

- pages
- layouts
- component hierarchy
- hooks
- state management

---

## Step 2 — Generate Layouts

Create layout containers.

Example:

layouts/MainLayout.tsx
layouts/AuthLayout.tsx

---

## Step 3 — Generate Pages

Create pages defined in the architecture.

Example:

pages/dashboard.tsx  
pages/projects.tsx  
pages/tasks.tsx

---

## Step 4 — Generate Components

Create reusable components.

components/Navbar.tsx  
components/ProjectCard.tsx  
components/TaskForm.tsx

---

## Step 5 — Generate Hooks

Create hooks for API interaction.

hooks/useProjects.ts  
hooks/useTasks.ts

---

## Step 6 — API Client

Create request utilities.

lib/apiClient.ts

---

## Step 7 — Apply Design Tokens

Use design tokens for:

- colors
- spacing
- typography

---

## Step 8 — Validation

Verify:

- pages match architecture
- components follow hierarchy
- API calls exist
