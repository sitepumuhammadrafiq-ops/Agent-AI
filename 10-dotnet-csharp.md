---
name: .NET and C# Conventions
description: Safe C# and .NET practices aligned with the repository's existing style.
---

# .NET and C#

- Verify `TargetFramework`, SDK pinning, nullable settings, language version, analyzers, and central package management before proposing syntax or package changes.
- Use asynchronous APIs for I/O when supported; propagate `CancellationToken` where the surrounding convention supports it.
- Avoid `.Result`, `.Wait()`, `async void` (except framework event handlers), fire-and-forget work, and broad exception swallowing.
- Preserve established dependency-injection lifetimes. Do not inject scoped services into singletons.
- Use structured logging; do not log secrets, credentials, tokens, full sensitive payloads, or unnecessary personal data.
- Keep methods cohesive. Avoid speculative abstractions and premature generic frameworks.
- Handle nullability explicitly; do not silence warnings with `!` without a demonstrated invariant.
- Respect existing naming, folder, namespace, and file organization.
- Add or update tests where test infrastructure exists and the change has meaningful behavior.
- Avoid changing target frameworks or major package versions as part of an unrelated feature.
