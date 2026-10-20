# Install and bootstrap checklist

## Before enabling
- [ ] Copy `.agents/` to the repository root.
- [ ] If a `.agents/` directory already exists, merge carefully and preserve local rules.
- [ ] Confirm the Antigravity version recognizes project rules, workflows, skills, and agent definitions.
- [ ] Confirm the repository root is the workspace root.
- [ ] Review `.agents/rules/00-oasis-core.md` and amend only facts verified from the codebase.

## First repository reconnaissance (read-only)
- [ ] Locate `.sln` / `.slnx`, `.csproj`, `global.json`, `Directory.Build.*`, `Directory.Packages.props`, `NuGet.config`.
- [ ] Identify Client, Server, Shared projects by their actual project files/namespaces.
- [ ] Check target frameworks and package versions; do not infer them from this bundle.
- [ ] Find existing patterns for API calls, dependency injection, DTOs, validation, error handling, auth, logging, and configuration.
- [ ] Identify database technology/access layer, migration mechanism, and transaction patterns.
- [ ] Find Hangfire registration, storage, recurring-job definitions, time zone, retry, and dashboard authorization.
- [ ] Find existing tests and exact build/test commands.
- [ ] Record warnings separately from errors and distinguish baseline warnings from introduced warnings.

## Verification
- [ ] Run a safe baseline build/test only after discovering the intended command.
- [ ] Never run a command that may modify production data or deploy.
- [ ] For browser-WASM projects, verify the correct project/solution and configuration; do not assume a publish command.
- [ ] For Telerik changes, use package APIs actually available in the installed version.
- [ ] Review `git diff` and ensure unrelated files are untouched.

## Completion report
- [ ] Summarize files changed and behavior changed.
- [ ] List exact commands run and their outcomes.
- [ ] State tests/builds not run and why.
- [ ] State remaining risks or follow-up work.
