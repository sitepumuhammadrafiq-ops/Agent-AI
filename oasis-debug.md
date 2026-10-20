---
description: Diagnose an OASIS bug from evidence before making a minimal fix.
---

# /oasis-debug

1. Capture the exact error, reproduction steps, expected behavior, and actual behavior.
2. Locate the failing path and trace relevant callers/dependencies.
3. Form ranked hypotheses with evidence; do not guess based only on the error message.
4. Reproduce safely if possible. Check logs and configuration without exposing secrets.
5. Identify the root cause before changing code.
6. Make the smallest fix and add a regression test where feasible.
7. Run the narrowest test/build that proves the fix, then broader verification if safe.
8. Explain root cause, fix, evidence, and residual uncertainty.
