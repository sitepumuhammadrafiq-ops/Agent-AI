---
name: Server Data and Hangfire
description: Server-side API, SQL Server, persistence, and background-job safety.
---

# Server, SQL Server, and Hangfire

- Server endpoints are the trust boundary: validate inputs and enforce authentication/authorization on the server.
- Follow the repository's existing data-access technology and transaction conventions. Do not introduce EF Core, Dapper, raw ADO.NET, or another ORM unless already used or explicitly approved.
- Use parameterized queries when SQL is written directly. Never concatenate untrusted input into SQL.
- Avoid loading unbounded result sets; use existing paging/filtering conventions.
- Treat schema changes as high impact: inspect migration conventions, compatibility, rollback strategy, and deployment order. Never apply migrations to a real environment without approval.
- For Hangfire, inspect existing registration, storage, serialization, retry policies, queues, time zone, recurring-job IDs, and dashboard authorization before editing.
- Background jobs should be idempotent where practical, have bounded retries, structured logs, and explicit handling for transient/permanent failures.
- Do not enqueue a job that performs real-world or data-changing work during verification unless the user explicitly approves.
- Never expose Hangfire Dashboard publicly without the existing authentication/authorization mechanism.
- Keep credentials in the established secure configuration mechanism; never commit secrets.
