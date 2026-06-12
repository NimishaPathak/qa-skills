---
name: rtm-creator
description: Use this skill whenever the user wants to create a Requirements 
  Traceability Matrix (RTM). Trigger for requests like "create RTM", "build 
  traceability matrix", "map test cases to requirements", or "link bugs to 
  test cases". Input will be an existing test case list and bug report.
---
# RTM Creator

## Purpose
Create a Requirements Traceability Matrix that maps:
- Requirements → Test Cases → Execution Status → Bugs Found

This ensures every requirement is tested and every bug is linked
to the test case that caught it.

## Inputs Required
Before creating the RTM, confirm you have:
1. Test Cases list — with TC ID, Module, Test Description, Status
2. Bug Report — with Bug ID, Severity, Linked TC ID, Status
3. Requirements list — if not available, derive from module names

If any input is missing, ask the user before proceeding.

## RTM Structure
Create the RTM with exactly these columns in this order:

| Column | Description |
|---|---|
| Requirement ID | Format: REQ-001, REQ-002 |
| Requirement Description | What the feature/module should do |
| Module | Which module this belongs to |
| TC ID | Test Case ID linked to this requirement |
| Test Description | One line summary of the test case |
| Execution Status | Pass / Fail / Not Executed |
| Bug ID | BUG-001 format, leave blank if no bug |
| Bug Severity | Critical / High / Medium / Low |
| Remarks | Any additional notes |

## Rules
Follow these strictly when creating the RTM:
1. Every module must have at least one REQ entry
2. Every TC ID must map to exactly one Requirement ID
3. If one requirement has multiple test cases, repeat the 
   requirement row for each TC ID
4. If a test case has no bug, leave Bug ID and Bug Severity blank
5. If execution status is not provided, mark as Not Executed
6. Do not skip any module from the test case list
7. Keep Requirement Description simple — one clear sentence

## Output Format
1. Produce the RTM as a Markdown table first for review
2. After user confirms, generate the RTM as a downloadable 
   .xlsx file with proper column headers and formatting
3. Group rows by Module — same module rows together
4. Sort modules in this order if working on OpenCart:
   Registration, Login, Forgot Password, Homepage, Search, 
   Product Detail, Cart, Checkout, Currency, Wishlist, My Account
5. At the end, provide a summary:
   - Total Requirements covered
   - Total Test Cases mapped
   - Total Bugs found
   - Modules with no bugs
   - Modules with failed test cases