---
name: run-tests
description: Execute the project’s automated test suite and prepare the test environment if required.
---

# Run Tests

Execute the automated test suite and generate a structured test report.

This skill must:

1. Detect the correct testing framework
2. Ensure test configuration exists
3. Run the tests
4. Write results to the validation report directory

---

# Inputs

Read the following project files if present:

- docs/reference/stack.md
- package.json
- requirements.txt
- go.mod
- pubspec.yaml

Detect project language and framework.

---

# Step 1 — Detect Project Stack

Determine the project stack.

Possible stacks:

Node / TypeScript  
Python  
Go  
React Native  
Flutter  
Swift  
Kotlin  

Use indicators such as:

package.json → Node ecosystem  
requirements.txt → Python  
go.mod → Go  
pubspec.yaml → Flutter  

---

# Step 2 — Detect Test Framework

Choose the correct framework based on the stack.

Node:

Vitest (preferred)  
Jest  
Playwright (E2E)

Python:

Pytest

Go:

Go test

Mobile:

React Native → Jest  
Flutter → Flutter test  
Swift → XCTest  
Kotlin → JUnit

---

# Step 3 — Ensure Test Configuration

If configuration files are missing, generate them automatically.

Examples:

Node:

vitest.config.ts  
tests/setup.ts  
.env.test  

Python:

pytest.ini  
tests/conftest.py  
.env.test  

Mobile:

appropriate test runner configuration

---

# Step 4 — Ensure Test Directory Exists

Ensure the following structure exists:

tests/

tests/unit  
tests/api  
tests/integration  
tests/mocks  
tests/utils  

Create directories if missing.

---

# Step 5 — Execute Test Suite

Run the appropriate command.

Examples:

Node:

npm test

Python:

pytest

Go:

go test ./...

Flutter:

flutter test

---

# Step 6 — Capture Results

Record:

- total tests executed
- passed tests
- failed tests
- failing files
- error messages

---

# Step 7 — Generate Test Report

Write results to:

validation-reports/test-results.json

Example structure:

{
  "status": "fail",
  "total": 48,
  "passed": 44,
  "failed": 4,
  "failures": [
    {
      "test": "projectService.test.ts",
      "error": "Expected 200 but received 500"
    }
  ]
}

---

# Step 8 — Output Status

If all tests pass:

All tests passed.

If failures exist:

Test failures detected.
