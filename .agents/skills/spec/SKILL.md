---
name: spec
description: "Create a focused feature specification before implementation."
---

# $spec — Specification-Driven Development

> "Plan the work, then work the plan."

## Purpose

Create a focused specification when the change needs explicit requirements, boundaries, or acceptance criteria. Ask only for details that materially affect the result; use clearly stated assumptions for the rest.

## Workflow

### Phase 1: Discovery (Ask Questions)

Before writing, inspect available project context. Ask only questions whose answers materially change the specification; state reasonable assumptions for the rest.

**Scope**
- What is the objective of this feature?
- Who are the target users?
- What problem does this solve?

**Features**
- What are the core features (MVP)?
- What are the acceptance criteria for each?
- What is explicitly out of scope?

**Technical**
- Any tech stack preferences or constraints?
- Integration points with existing systems?
- Performance requirements?

### Phase 2: Generate Specification

After discovery, produce `SPEC.md` with these sections:

```markdown
# Feature: [Name]

## Objective
[1-2 sentences describing the goal]

## Target Users
[Who will use this and why]

## Core Features
1. [Feature A] — [Acceptance criteria]
2. [Feature B] — [Acceptance criteria]
3. [Feature C] — [Acceptance criteria]

## Out of Scope
- [What we're NOT building in this iteration]

## Technical Approach
- Tech stack decisions
- Data models
- API contracts (if applicable)
- Integration points

## Code Style
- Follow rules in `../../references/rules/`
- [Any feature-specific conventions]

## Testing Strategy
- Unit tests for: [areas]
- Integration tests for: [areas]
- E2E tests for: [critical paths]

## Boundaries
### Always Do
- [Non-negotiables]

### Ask First
- [Decisions requiring approval]

### Never Do
- [Hard constraints]
```

### Phase 3: Review and next step

- Present the spec and call out assumptions
- Continue to `$plan` when requested, or when the user has already asked for implementation and no unresolved decision blocks progress
- Save as `SPEC.md` in the project root or `docs/specs/[feature].md`

## Output

- `SPEC.md` — The specification document
- Clear alignment on what to build

## Next Step

When implementation is requested, continue to `$plan` to decompose the work into tasks.
