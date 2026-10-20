---
name: OASIS Core Engineering Rules
description: Non-negotiable project-wide engineering constraints for OASIS.
---

# OASIS core rules

1. **Inspect before changing.** Read the target files and adjacent implementations, project files, relevant services/DTOs, and tests before editing.
2. **Preserve the existing architecture.** OASIS is expected to use .NET 8, Blazor WebAssembly Hosted, Telerik UI for Blazor 10.0.0, SQL Server, and Hangfire, with Client/Server/Shared boundaries. Treat these as user-provided targets, then verify the actual repository. Do not invent or rename project boundaries.
3. **Follow local precedent.** Existing working patterns are the source of truth. Prefer the smallest coherent change over a broad refactor.
4. **Respect boundaries.** Client code must not access SQL Server directly or reference server-only implementation details. Shared contracts must remain suitable for every project that references them. Server owns privileged operations and database access.
5. **Do not fabricate APIs.** Confirm framework, package version, namespaces, component parameters, and method signatures from the codebase or installed package documentation.
6. **Keep changes scoped.** Do not reformat or refactor unrelated files. Avoid new dependencies unless necessary and justified.
7. **Security by default.** Never expose secrets or sensitive configuration. Validate untrusted input on the server; do not rely on client-side validation as a security boundary. Enforce authorization at server endpoints/jobs.
8. **No destructive actions without approval.** Do not run production migrations, data deletion, data repair, deployment, credential rotation, or commands with irreversible side effects without explicit approval.
9. **Verify honestly.** Never claim a build, test, browser check, or runtime check passed unless it was actually run and its exit/result inspected.
10. **Report uncertainty.** If the repository contradicts an assumption here, explain the discrepancy and follow verified codebase facts unless the user explicitly directs otherwise.
