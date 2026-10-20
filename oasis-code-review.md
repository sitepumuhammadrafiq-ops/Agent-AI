---
description: Review current OASIS changes for correctness, regressions, security, and maintainability.
---

# /oasis-code-review

Review the diff, not just the final files.

Prioritize findings:
- P0: critical security/data-loss/outage risk
- P1: likely bug, authorization failure, broken core flow, or serious regression
- P2: meaningful correctness/maintainability issue
- P3: minor improvement or style inconsistency

For every finding, include severity, file/line, concrete scenario, impact, and recommended fix.
Check architecture boundaries, API contracts, null/error handling, async behavior, SQL safety,
authorization, Hangfire retries/idempotency, Telerik version compatibility, accessibility, and tests.
Do not report speculative issues as confirmed. If no findings, state what was reviewed and what was not verified.
Do not modify code unless asked to fix findings.
