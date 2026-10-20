---
name: Change Control
description: Risk controls for agent-driven code changes.
---

# Change control

- Start with a concise plan for multi-file, architectural, security, data, or background-job changes.
- Ask before broad refactors, public contract changes, package upgrades, target framework changes, schema/data changes, deployments, or changes with significant operational impact.
- Do not overwrite user changes. Inspect working-tree status and diff before editing when git is available.
- Do not delete files or generated assets unless they are clearly obsolete and deletion is in scope.
- Do not edit `bin/`, `obj/`, generated clients, minified assets, or lock files manually unless the repository workflow requires it.
- Keep secrets and personal/customer data out of logs, fixtures, commits, reports, and prompts.
- If an instruction conflicts with repository security or destructive-action safeguards, stop and ask for clarification.
