---
description: Investigate .NET/Blazor WebAssembly build size or performance with measurements first.
---

# /oasis-optimize-build

1. Clarify whether the target is build duration, output size, download size, startup, runtime CPU/memory, or server latency.
2. Capture baseline measurements using the existing build/publish configuration.
3. Identify actual output directories and classify files by extension/size; distinguish raw, compressed, and published output.
4. Inspect project references, package references, linker/trimmer settings, globalization, static assets, and Telerik usage.
5. Make one evidence-backed change at a time; avoid speculative package removal or linker directives.
6. Rebuild with the same configuration and compare like-for-like measurements.
7. Verify runtime behavior, especially reflection, serialization, localization, Telerik components, and dynamically loaded code.
8. Report baseline, change, after measurement, tradeoffs, commands, and remaining uncertainty.
9. Do not alter framework/package versions or deployment compression settings without explaining impact and getting approval when material.
