---
name: test-case-creator
description: Use this skill whenever the user wants to create test cases,
  write test scenarios, or plan test coverage for any module, page, or
  feature. Trigger for requests like "write test cases for login", "create
  test scenarios for dashboard", "give me test coverage for registration page",
  or "create test cases for OrangeHRM". Works for web, mobile, and API testing.
---

# Test Case Creator

## Purpose
Create comprehensive, professional test cases that cover:
- Functional correctness of features
- Positive, negative and edge case scenarios
- Boundary value analysis
- UI validation and error message verification

## Inputs Required
Before creating test cases, confirm you have:
1. Application name and URL
2. Module or page name to test
3. Feature description or requirements if available
4. Any existing test cases to avoid duplication

If inputs are missing, derive from application context
or ask the user before proceeding.

## Test Case Structure
Every test case must follow this exact format:

| Field | Description |
|---|---|
| TC ID | Format: TC_MODULE_001 (e.g. TC_LOG_001) |
| Module | Page or feature name |
| Test Description | One clear sentence of what is being tested |
| Preconditions | What must be true before executing |
| Test Steps | Numbered steps, each action on a new line |
| Expected Result | What should happen if feature works correctly |
| Actual Result | Leave blank — filled during execution |
| Status | Leave blank — Pass/Fail filled during execution |
| Priority | High / Medium / Low |
| Test Type | Positive / Negative / Edge Case 
|

## Coverage Rules
Always cover these for every module:
1. Happy path — valid inputs, expected successful flow
2. Negative cases — invalid inputs, wrong credentials,
   empty fields, special characters
3. Boundary values — max/min character limits,
   numeric boundaries
4. Edge cases — spaces, special characters, very long
   inputs, copy-paste behavior
5. UI validation — error messages, field labels,
   placeholder text, mandatory field indicators
6. Navigation — breadcrumbs, page titles, redirects
   after actions

Minimum test cases per module:
- Simple module (e.g. Forgot Password): 5-8 TCs
- Medium module (e.g. Login): 8-12 TCs
- Complex module (e.g. Registration, Checkout): 10-15 TCs

## Output Format
1. Generate test cases as a .xlsx file
2. Use this filename: TestCases-[ProjectName]-v1.0.xlsx
3. Create one sheet per module
4. Apply these formatting rules:
   - Header row: bold, blue background, white text
   - Alternate row colors for readability
   - Auto-fit all column widths
   - Freeze top row
   - Add borders to all cells
5. Add a Summary sheet with:
   - Total modules covered
   - Total test cases per module
   - Grand total test cases
6. Save directly into the Test-Cases folder
   of the current project
7. Group test cases in this order per sheet:
   Positive Tests → Negative Tests → Edge Cases