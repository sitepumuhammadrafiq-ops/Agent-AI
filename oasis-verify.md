---
description: Run repository-appropriate, safe verification and report evidence accurately.
---

# /oasis-verify

1. Discover solution/project files, SDK, test projects, and documented build commands.
2. Check `git status` and do not overwrite existing changes.
3. Run focused tests first if relevant.
4. Run the correct build command for the affected project/configuration; avoid guessing project names.
5. If relevant and safe, run `git diff --check` and inspect the full diff.
6. Do not deploy, run production migrations, alter production data, or execute real background jobs.
7. Report each command and pass/fail/blocked status, including exit code when available.
8. Explicitly distinguish compile verification from runtime/browser verification.
