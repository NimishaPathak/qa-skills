---
name: readme-creator
description: Use this skill whenever the user wants to create a README.md
  file for a GitHub repository. Trigger for requests like "create README",
  "write README for my project", "generate GitHub README", or "add README
  to my repo". Works for manual testing, automation, and API testing projects.
---

# README Creator

## Purpose
Create a professional GitHub README.md file that:
- Clearly explains the project to clients and recruiters
- Shows tools, tech stack, and domain expertise
- Lists all deliverables with status
- Demonstrates QA thought process and coverage

## Inputs Required
Before creating the README, confirm you have:
1. Project type — Manual Testing / API Testing / Automation
2. Application name and URL
3. Domain — E-Commerce / HR SaaS / API
4. Modules tested — list of module names
5. Deliverables list — what documents are completed
6. Tools used — browser, OS, test tools, frameworks
7. Bugs found — Bug ID, summary, severity

If any input is missing, derive from project files provided
or ask the user before proceeding.

## README Structure
Create the README with exactly these sections in this order:

1. Project Title and Badges
   - Project name as H1 heading
   - Badges for: Manual Testing, domain, status (Completed)

2. Project Overview
   - 2-3 sentences describing what was tested and why

3. Application Under Test
   - App name, URL, type, domain

4. Test Coverage Table
   - Module name and test case count per module
   - Total row at the bottom

5. Deliverables Table
   - Document name and status (✅ Done / 🔄 In Progress / ⏳ Pending)

6. Bugs Found Table
   - Bug ID, summary, severity

7. Test Execution Summary
   - Total TCs, Passed, Failed, Pass Percentage
   - Final recommendation

8. Tools Used
   - Testing tools, browser, OS, bug tracking

9. Author
   - Name and title

## Rules
Follow these strictly when creating the README:
1. Always use proper Markdown formatting — headers, tables, badges
2. Badges must use shields.io format:
   ![Badge](https://img.shields.io/badge/label-value-color)
3. Keep Project Overview professional — no first person language
4. Deliverables table must show exact status from user input
5. Bug table must match exactly with bug report provided
6. Test Execution Summary numbers must match test cases provided
7. Author section must use exact name provided by user
8. Keep language concise — no unnecessary filler sentences
9. README must work for both manual and automation projects
10. For automation projects add extra section — Framework Architecture

## Output Format
1. Produce the README as a .md file
2. Use this filename: README.md
3. Save directly into the root of the current project folder
4. After generating, show a preview of the top section
   in the chat so user can verify before committing
5. Use this structure for badges at the top:
   - Testing Type badge
   - Domain badge  
   - Status badge
   - Test Cases count badge
6. All tables must be properly aligned in Markdown
7. Do not add any sections not listed in README Structure
8. Keep the file clean — no HTML tags, pure Markdown only