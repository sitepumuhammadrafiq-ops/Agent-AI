---
description: Safely inspect or modify Hangfire jobs in OASIS.
---

# /oasis-hangfire-change

1. Identify current Hangfire registration, storage, queues, serializer compatibility, dashboard auth, and recurring-job definitions.
2. Confirm whether the requested job is recurring, delayed, scheduled, or fire-and-forget.
3. Inspect existing job method signatures and dependency lifetimes.
4. Design for idempotency, bounded retries, observability, cancellation/timeout where supported, and safe failure handling.
5. Do not trigger real jobs or modify recurring schedules in a live environment without explicit approval.
6. For schedule changes, state the time zone and behavior around daylight-saving/time-zone configuration as relevant.
7. Verify registration/configuration through safe tests or build; do not claim execution success if the job was not executed.
8. Report operational risks and rollback considerations.
