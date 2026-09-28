# AI Agent Project — Production-Grade Configuration

<div align="center">
  <img src="https://res.cloudinary.com/ecommerce2021/image/upload/v1768626951/dev_efjbzw.jpg" alt="Code Web Khong Kho" width="120" style="border-radius: 50%"/>

  <h3>Production-ready AI Agent configuration for Claude Code and Codex</h3>
  <p>Structured workflows, specialized agents, mandatory rules, and best practices</p>

  ![Version](https://img.shields.io/badge/version-1.2.0-blue?style=flat-square)
  [![Facebook](https://img.shields.io/badge/Facebook-Code%20Web%20Khong%20Kho-1877F2?logo=facebook)](https://www.facebook.com/codewebkhongkho)
  [![TikTok](https://img.shields.io/badge/TikTok-@code.web.khng.kh-000000?logo=tiktok)](https://www.tiktok.com/@code.web.khng.kh)
  [![Website](https://img.shields.io/badge/Website-codewebkhongkho.com-FF6B35?logo=google-chrome)](https://codewebkhongkho.com/portfolios)

  <sub>Inspired by <a href="https://github.com/addyosmani/agent-skills">addyosmani/agent-skills</a></sub>
</div>

---

## Overview

This repository provides structured AI development workflows for **Claude Code and Codex**. It includes:

- **Structured development workflow** (Spec → Plan → Build → Test → Review → Ship)
- **10 specialized agents** for different development roles
- **13 coding rules** covering code quality, architecture, and operations
- **9 workflow commands** for common development tasks
- **13 Codex skills** and **10 project-scoped Codex agents**
- **4 reference checklists** for security, testing, performance, and accessibility

---

## Claude Code Workflow

Use slash commands in Claude Code. Codex provides the same workflows as skills, invoked with `$skill-name`.

```
┌──────────────────────────────────────────────────────────────────┐
│                                                                  │
│   /spec  →  /plan  →  /build  →  /test  →  /review  →  /deploy  │
│                                                                  │
│   Define    Plan     Build     Verify    Review      Ship        │
│                                                                  │
└──────────────────────────────────────────────────────────────────┘
```

| Phase | Command | Description |
|-------|---------|-------------|
| **Define** | `/spec` | Create PRD with objectives, scope, and boundaries |
| **Plan** | `/plan` | Decompose into vertical slices with acceptance criteria |
| **Build** | `/build` | Implement incrementally using TDD |
| **Verify** | `/test` | Write tests with RED-GREEN-REFACTOR |
| **Review** | `/review` | Five-axis code review |
| **Ship** | `/deploy` | Build, test, and deploy |

### Supporting Commands

| Command | Description |
|---------|-------------|
| `/debug` | Systematic error diagnosis |
| `/simplify` | Reduce code complexity |
| `/fix-issue` | Analyze and fix issues |

---

## Project Structure

### Codex

```
.agents/                         # Codex skills and reference material
├── skills/                      # 13 reusable workflows
└── references/
    ├── rules/                   # 13 portable coding rules
    └── checklists/              # 4 portable checklists

.codex/
└── agents/                      # 10 Codex subagents (*.toml)

AGENTS.md                       # Codex project instructions
```

### Claude Code

```
.claude/
├── CLAUDE.md                    # Main AI configuration
│
├── commands/                    # Slash commands (9 total)
│   ├── spec.md                  # /spec — PRD creation
│   ├── plan.md                  # /plan — Task breakdown
│   ├── build.md                 # /build — Incremental implementation
│   ├── test.md                  # /test — TDD workflow
│   ├── review.md                # /review — Code review
│   ├── deploy.md                # /deploy — Deployment
│   ├── debug.md                 # /debug — Error diagnosis
│   ├── simplify.md              # /simplify — Code simplification
│   └── fix-issue.md             # /fix-issue — Issue resolution
│
├── agents/                      # Specialized agents (10 total)
│   ├── frontend.md              # Frontend Developer
│   ├── backend.md               # Backend Developer
│   ├── systems-architect.md     # Systems Architect
│   ├── code-reviewer.md         # Code Reviewer
│   ├── test-engineer.md         # Test Engineer
│   ├── security-auditor.md      # Security Auditor
│   ├── qa.md                    # QA Engineer
│   ├── project-manager.md       # Project Manager
│   ├── ui-ux-designer.md        # UI/UX Designer
│   └── copywriter-seo.md        # Copywriter/SEO
│
├── rules/                       # Mandatory rules (13 total)
│   ├── clean-code.md            # Clean Code principles
│   ├── code-style.md            # Formatting & naming
│   ├── error-handling.md        # Error patterns
│   ├── tech-stack.md            # Approved technologies
│   ├── system-design.md         # System design patterns
│   ├── project-structure.md     # Folder organization
│   ├── api-conventions.md       # REST API standards
│   ├── naming-conventions.md    # Naming patterns
│   ├── database.md              # Database patterns
│   ├── security.md              # Security requirements
│   ├── monitoring.md            # Observability
│   ├── testing.md               # Test standards
│   └── git-workflow.md          # Git conventions
│
├── skills/                      # Advanced skills (5 total)
│   ├── tdd/SKILL.md             # Test-Driven Development
│   ├── code-review/SKILL.md     # Five-axis review
│   ├── incremental-implementation/SKILL.md
│   ├── deploy/SKILL.md
│   └── security-review/SKILL.md
│
├── references/                  # Quick checklists
│   ├── security-checklist.md
│   ├── testing-patterns.md
│   ├── performance-checklist.md
│   └── accessibility-checklist.md
│
└── settings.json                # Project settings
```

The files under `.agents/references/` are Codex-ready copies of `.claude/rules/` and `.claude/references/`. Keep corresponding files in sync when updating the shared guidance.

---

## Specialized Agents

### Development Agents

| Agent | Role | Invoke When |
|-------|------|-------------|
| **Frontend Developer** | Next.js, React, TypeScript, UI | Components, pages, state |
| **Backend Developer** | Express, Prisma, Redis, BullMQ | APIs, services, jobs |
| **Systems Architect** | Architecture, ADRs, scaling | System design decisions |

### Quality Agents

| Agent | Role | Invoke When |
|-------|------|-------------|
| **Code Reviewer** | Five-axis code review | PR reviews, quality checks |
| **Test Engineer** | TDD, coverage, test strategy | Writing and reviewing tests |
| **Security Auditor** | Vulnerability, threat modeling | Security reviews |
| **QA Engineer** | Test plans, E2E, bug reports | Quality assurance |

### Product Agents

| Agent | Role | Invoke When |
|-------|------|-------------|
| **Project Manager** | Stories, sprints, planning | Project planning |
| **UI/UX Designer** | Design system, accessibility | UX decisions |
| **Copywriter/SEO** | Copy, meta tags, SEO | Content creation |

---

## Recommended Tech Stack

Use these choices as defaults for new projects. An existing repository's documented stack and the user's requirements take priority.

| Layer | Technology |
|-------|-----------|
| **Frontend (SEO)** | Next.js 14 (App Router) |
| **Frontend (Admin)** | React + Vite |
| **Styling** | Tailwind CSS + shadcn/ui |
| **State** | Zustand + TanStack Query |
| **Backend** | Express.js + TypeScript |
| **ORM** | Prisma |
| **Database** | PostgreSQL |
| **Cache** | Redis (ioredis) |
| **Queue** | BullMQ (simple) / RabbitMQ (enterprise) |
| **Auth** | NextAuth.js / JWT + bcrypt |
| **Testing** | Vitest + Playwright |
| **Monitoring** | Prometheus + Grafana + Pino |
| **CI/CD** | GitHub Actions |
| **Deploy** | Vercel + Railway/Fly.io |

---

## Mandatory Rules

The 13 rules are available in `.claude/rules/` for Claude Code and in `.agents/references/rules/` for Codex. Treat the stack and architecture examples as defaults to adapt to the target project's existing instructions and technology choices.

### Code Quality
- **clean-code.md** — Variables, functions, SOLID, async/await
- **code-style.md** — 2-space indent, single quotes, semicolons
- **error-handling.md** — AppError class, centralized handler

### Architecture
- **tech-stack.md** — Approved technologies only
- **system-design.md** — CAP, caching, scaling patterns
- **project-structure.md** — Layered architecture
- **api-conventions.md** — REST standards, response envelopes

### Data & Naming
- **naming-conventions.md** — Cache keys, DB, queues, env vars
- **database.md** — Prisma patterns, N+1 prevention

### Operations
- **security.md** — **CRITICAL** — Never violate
- **monitoring.md** — Prometheus, Grafana, alerting
- **testing.md** — 80% coverage minimum
- **git-workflow.md** — Conventional commits

---

## Quick Start

```bash
# Clone repository
git clone <repo-url>
cd ai-agent

# Claude Code
cp -r .claude/ /path/to/your/project/

# Codex
cp AGENTS.md /path/to/your/project/
cp -r .agents/ /path/to/your/project/
cp -r .codex/ /path/to/your/project/

# Or use as template
```

### Using Commands

```bash
# In Claude Code, use slash commands:
/spec "User authentication feature"
/plan
/build
/test
/review
/deploy
```

In Codex, invoke the corresponding skill with `$spec`, `$plan`, `$build`, `$test`, `$review`, `$deploy`, `$debug`, `$simplify`, or `$fix-issue`. The additional skills are `$tdd`, `$code-review`, `$incremental-implementation`, and `$security-review`. Type `$` to browse available skills. Codex also has built-in `/plan` and `/review` commands.

Codex loads project guidance from `AGENTS.md`, skills from `.agents/skills/`, and custom subagents from `.codex/agents/`. The Codex agent files use these IDs: `frontend_developer`, `backend_developer`, `systems_architect`, `code_reviewer`, `test_engineer`, `security_auditor`, `qa_engineer`, `project_manager`, `ui_ux_designer`, and `copywriter_seo`. Codex project agents and project-scoped configuration require the repository to be trusted. See the [Codex AGENTS.md guide](https://learn.chatgpt.com/docs/agent-configuration/agents-md), [skills guide](https://learn.chatgpt.com/docs/build-skills), and [subagents guide](https://learn.chatgpt.com/docs/agent-configuration/subagents).

### Using Agents

```
"Act as the Frontend Developer and build the login page"
"As Systems Architect, design the notification system"
"Code Reviewer: review this PR for security issues"
"Test Engineer: write tests for the payment flow"
```

---

## Key Concepts

### Five-Axis Code Review

Every code review evaluates:

1. **Correctness** — Does it work? Edge cases?
2. **Readability** — Can others understand it?
3. **Architecture** — Follows patterns? Appropriate abstractions?
4. **Security** — Input validation? Auth? No secrets?
5. **Performance** — N+1? Pagination? Async?

### Test-Driven Development

```
RED    → Write failing test
GREEN  → Write minimal code to pass
REFACTOR → Improve while green
```

### Vertical Slicing

Build features end-to-end, not layer-by-layer:

```
✅ Task 1: User can create task (DB + API + UI)
✅ Task 2: User can view tasks (DB + API + UI)

❌ Task 1: Create all DB models
❌ Task 2: Create all API routes
```

---

## Security

**Never commit:**
- Runtime environment files such as `.env` or `.env.production` (keep `.env.example` free of real secrets)
- API keys, secrets, passwords
- `.claude/settings.local.json` and `.claude/CLAUDE.local.md`

**Always:**
- Use environment variables
- Validate all inputs
- Hash passwords (bcrypt >= 12 rounds)
- Parameterize queries

---

## Contributing

1. Follow the development workflow (`/spec` → `/plan` → `/build` in Claude Code, or `$spec` → `$plan` → `$build` in Codex)
2. Ensure all tests pass
3. Run `/review` in Claude Code; in Codex, use the built-in `/review` or the project `$review` skill
4. Follow conventional commit format

---

## Credits

- Workflow inspired by [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills)
- Best practices from *Software Engineering at Google*
- Clean Code principles from Robert C. Martin

---

## Author

<div align="center">
  <img src="https://res.cloudinary.com/ecommerce2021/image/upload/v1768626951/dev_efjbzw.jpg" alt="Code Web Khong Kho" width="80" style="border-radius: 50%"/>

  **Code Web Khong Kho**

  | Platform | Link |
  |----------|------|
  | Facebook | [facebook.com/codewebkhongkho](https://www.facebook.com/codewebkhongkho) |
  | TikTok | [@code.web.khng.kh](https://www.tiktok.com/@code.web.khng.kh) |
  | Website | [codewebkhongkho.com](https://codewebkhongkho.com/portfolios) |
</div>

---

<div align="center">
  <sub>Made with care by <a href="https://www.facebook.com/codewebkhongkho">Code Web Khong Kho</a></sub>
</div>
