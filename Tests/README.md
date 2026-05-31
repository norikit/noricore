# Tests

Tests live here, mirroring the structure of `Sources/`.

- Unit tests exercise individual providers and broker logic in isolation (use mock system
  APIs where necessary to avoid hardware/system dependencies in CI).
- Integration tests can exercise the full broker + transport stack in a headless mode.

The headless self-test path (`--self-test` in the daemon entry point) is the CI-runnable
smoke check; this directory is for the full test suite.

> Delete or trim this README once real tests exist.
