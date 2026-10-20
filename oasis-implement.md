---
description: Implement a scoped OASIS change following existing project patterns and verify it.
---

# /oasis-implement

1. Read the task plan if one exists; otherwise create a short plan first.
2. Inspect current working-tree changes and all relevant source files.
3. Confirm the target project, target framework, package APIs, and analogous code.
4. Implement the smallest complete change. Preserve Client/Server/Shared boundaries.
5. Add/update tests if appropriate and possible.
6. Run focused verification, then broader safe build/test commands discovered in the repository.
7. Inspect diffs for scope creep, generated files, secrets, and regressions.
8. Report changed files, behavior, exact verification commands/results, and anything not verified.
9. Stop and ask before destructive operations, schema changes, deployments, or broad architecture changes.
