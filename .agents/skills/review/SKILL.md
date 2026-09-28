---
name: review
description: "Review a change for correctness, maintainability, architecture, security, and performance."
---

# $review — Code Review

## Description
Perform a thorough code review of specified files or a pull request.

## Usage
Use this skill when asked to perform the workflow described above.

## Review Checklist

### Code Quality
- [ ] Code follows style guide (`../../references/rules/code-style.md`)
- [ ] No unnecessary complexity or duplication
- [ ] Functions are small and focused (single responsibility)
- [ ] Variable and function names are descriptive

### Security
- [ ] No hardcoded secrets or credentials
- [ ] Input validation is present
- [ ] Authentication/authorization checks in place
- [ ] See `../../references/rules/security.md` for full checklist

### Error Handling
- [ ] Errors are properly caught and handled
- [ ] Meaningful error messages
- [ ] No swallowed exceptions
- [ ] See `../../references/rules/error-handling.md`

### Testing
- [ ] Unit tests cover new logic
- [ ] Edge cases are tested
- [ ] Tests are readable and maintainable
- [ ] See `../../references/rules/testing.md`

### Database
- [ ] Queries are optimized (no N+1)
- [ ] Transactions used where appropriate
- [ ] See `../../references/rules/database.md`

### API
- [ ] Endpoints follow REST conventions
- [ ] Request/response schemas are documented
- [ ] See `../../references/rules/api-conventions.md`

## Output Format
Provide feedback as:
- 🔴 **Critical** — Must fix before merge
- 🟡 **Warning** — Should fix, potential issue
- 🟢 **Suggestion** — Nice to have improvement
- ✅ **Good** — Highlight what's done well
