---
name: Testing and Verification
description: Required evidence and completion standards.
---

# Testing and verification

- Before editing, identify the correct solution/project and discover available tests and repository build conventions.
- Prefer focused tests first, then relevant project/solution verification if practical.
- Use the repository's existing test framework and naming patterns. Do not add a test framework solely for a tiny change without justification.
- For UI changes, compile the affected project and test loading, empty, error, validation, and interaction paths as relevant.
- For API/data changes, test validation, authorization, not-found behavior, failure paths, and serialization where appropriate.
- For Hangfire changes, verify job registration/metadata without executing unsafe production work.
- Capture exact commands and exit codes. If a command cannot run, say why and what remains unverified.
- Compare new warnings/errors against baseline when baseline evidence exists.
- Inspect `git diff --check` and `git diff`; look for secrets, accidental generated files, unrelated changes, and broken project references.
- A successful build does not prove runtime correctness. State verification level accurately.
