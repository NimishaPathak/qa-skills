---
name: test-summary-report
description: Use this skill whenever the user wants to create a Test Summary
  Report. Trigger for requests like "create test summary report", "generate
  test summary", "summarize testing results", or "write final test report".
  Input will be test cases, bug report, and RTM files.
---

# Test Summary Report Creator

## Purpose
Create a professional Test Summary Report that summarizes:
- Overall testing scope and objectives
- Test execution results
- Bugs found and their status
- Final quality assessment and sign-off recommendation

## Inputs Required
Before creating the report, confirm you have:
1. Test Plan — for scope, objectives, and environment details
2. Test Cases — with execution status (Pass/Fail/Not Executed)
3. Bug Report — with Bug ID, Severity, and Status
4. RTM — for requirements coverage summary

If any input is missing, ask the user before proceeding.

## Report Structure
Create the report with exactly these sections in this order:

1. Cover Information
   - Project Name
   - Application URL
   - Prepared By
   - Date
   - Version

2. Test Objective
   - One paragraph summarizing what was tested and why

3. Scope
   - Modules included in testing
   - Modules excluded from testing

4. Test Environment
   - OS, Browser, Application Version
   - Test Management Tool
   - Bug Tracking Tool

5. Test Execution Summary
   - Total Test Cases Written
   - Total Executed
   - Total Passed
   - Total Failed
   - Total Not Executed
   - Pass Percentage

6. Bug Summary
   - Total Bugs Found
   - Critical / High / Medium / Low count
   - Bug Status (Open / Fixed / Closed)

7. Module-wise Testing Status
   - Table showing each module with Pass/Fail/Not Executed counts

8. Observations and Recommendations
   - Key findings from testing
   - Risks identified
   - Recommendation — Pass / Fail / Conditional Pass

9. Sign-off
   - Prepared By
   - Reviewed By
   - Date

## Rules
Follow these strictly when creating the report:
1. Pass Percentage = (Total Passed / Total Executed) * 100
2. If Pass Percentage is above 90% recommend Pass
3. If Pass Percentage is between 70-90% recommend Conditional Pass
4. If Pass Percentage is below 70% recommend Fail
5. Never leave any section blank - write N/A if data not available
6. Bug Summary must match exactly with the Bug Report provided
7. Module-wise table must cover all modules from the test cases
8. Keep language formal and professional throughout
9. Version format: v1.0

## Output Format
1. Produce the report as a professional DOCX file
2. Use this filename: TestSummaryReport-[ProjectName]-v1.0.docx
3. Apply these formatting rules:
   - Title: Bold, 18pt, centered
   - Section headings: Bold, 14pt
   - Body text: 11pt, Calibri font
   - Tables: bordered, header row bold with blue background
   - Page margins: 1 inch all sides
4. Save the file directly into the Test-Summary-Report folder
   of the current project
5. After generating, provide a brief summary of key metrics
   in the chat