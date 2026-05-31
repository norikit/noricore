# Sources

Product code lives here. Organize it by **responsibility — one directory per architectural
layer**, each named for what it *does* (not by file type).

Planned layout (see [ai-docs/architecture.md](../ai-docs/architecture.md)):

```
Sources/noricore/
  Providers/   — system data source modules (Battery, Network, ActiveApp, …)
  Broker/      — event bus, topic registry, state cache, routing
  Transport/   — IPC layer (type TBD — see Q1 in ai-docs/open-questions.md)
  Schema/      — event type definitions and wire protocol
  Daemon/      — entry point: LaunchAgent lifecycle, signal handling, startup
```

Always keep:

- a **single, clear entry point** (`Daemon/main.swift`), and
- a **headless self-test path** (`--self-test` flag) that exercises core invariants without
  a display or window, so CI can run it.

Throwaway PoC/research code does **not** belong here — it lives in `tasks/<id>/code/`.

> Delete or trim this README once real source exists.
