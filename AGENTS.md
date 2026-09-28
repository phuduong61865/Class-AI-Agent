# Codex project instructions

This repository packages development guidance for Claude Code and Codex. When applying it to another repository, follow that repository's instructions and the user's request first. Treat this template's stack and architecture examples as defaults to adapt, not requirements that override an existing project.

## Working in this repository

- Read the applicable rule in `.agents/references/rules/` and checklist in `.agents/references/checklists/` for the task; keep unrelated references out of context.
- Discover the project's actual language, package manager, scripts, and conventions before choosing commands or changing structure. The examples in these guides often use TypeScript, Node.js, and npm.
- Use the matching skill under `.agents/skills/` for repeatable workflows. Codex can also load specialized agents from `.codex/agents/`; delegate to them by their configured name when useful.
- Make focused changes and report what you changed and which checks you ran. Never claim a check succeeded unless it did.
- Do not stage or commit changes, push branches, publish releases, deploy, or roll back unless the user explicitly asks. For production or rollback actions, make sure the target and procedure are clear.

## References

- Coding and architecture standards: `.agents/references/rules/`
- Security, testing, performance, and accessibility checklists: `.agents/references/checklists/`
- Codex workflows: `.agents/skills/`
- Codex specialist agents: `.codex/agents/`
