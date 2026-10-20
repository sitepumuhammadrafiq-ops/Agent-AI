---
name: Blazor and Telerik UI
description: UI implementation rules for OASIS Blazor WebAssembly and Telerik components.
---

# Blazor and Telerik UI

- Inspect comparable Razor components and their code-behind before creating a new pattern.
- Verify the installed Telerik UI for Blazor package version and use only APIs supported by that version. The target stated for this project is 10.0.0; repository package files take precedence if they differ.
- Preserve the project's established component composition, naming, CSS conventions, localization, loading, empty, error, and authorization states.
- Keep server-only logic and secrets out of WebAssembly code. Anything shipped to the browser is inspectable by the user.
- Use the existing API client/service layer; do not call database code from a component.
- Avoid unnecessary rerenders, repeated API requests, unbounded rendering, and expensive work in render paths.
- Follow existing disposal patterns for subscriptions, timers, cancellation sources, and event handlers.
- For Telerik Grid/forms/charts, inspect nearby implementations and confirm event types, data-binding mode, command behavior, and component parameters before coding.
- Keep accessibility in mind: labels, keyboard operation, meaningful status/error messages, and sensible focus behavior.
- Do not change global theme, Telerik version, or shared UI primitives to solve a local issue unless the impact is reviewed.
