---
name: fix-issue
description: "Investigate and fix a reported issue with a focused, verified change."
---

# Fix Issue Command

## Description
Analyze and fix a reported bug or issue systematically.

## Usage
Use this skill when asked to perform the workflow described above.

## Process

### 1. Understand the Issue
- Read the error message or bug description carefully
- Identify the affected component(s)
- Reproduce the issue locally if possible

### 2. Root Cause Analysis
- Check recent git changes: `git log --oneline -20`
- Review affected files
- Look for related tests that may reveal expected behavior

### 3. Plan the Fix
- Identify the minimal change needed
- Consider side effects on other components
- Update or add tests to cover the fix

### 4. Implement
- Make the targeted fix
- Ensure code follows `../../references/rules/code-style.md`
- Handle errors per `../../references/rules/error-handling.md`

### 5. Verify
- Run the smallest relevant verification command documented by the project, when appropriate.
- Run broader checks only when the task calls for them or the project workflow requires them.
- Run the project-documented lint command when relevant.

### 6. Commit (only if requested)
Follow `../../references/rules/git-workflow.md`:
```
fix: [short description of the fix]

Closes #[issue-number]
```
