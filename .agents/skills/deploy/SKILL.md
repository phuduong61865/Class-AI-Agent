---
name: deploy
description: "Prepare or perform a deployment using the target project instructions and an explicitly requested target."
---

# Deployment workflow

Use this skill when the user asks to prepare or perform a deployment.

1. Inspect the target project's deployment documentation, CI/CD configuration, package scripts, and environment setup. Identify the target environment and the actual deploy, health-check, and rollback procedures.
2. Before deployment, review the working tree and the relevant tests, lint, build, and migration checks documented by the project. Do not assume an npm command or a particular hosting platform.
3. Summarize readiness, blockers, and the exact target and commands you intend to use.
4. Deploy only when the user explicitly requested deployment and the target is clear. Do not push, publish a release, run production migrations, or roll back as an implied part of preparation.
5. After an explicitly requested deployment, perform only the documented post-deployment checks and report the observed result. Never report success without command or health-check evidence.

Read the adjacent `deploy.md` for deployment and CI/CD examples. Treat examples there as reference material and adapt them to the target project.
