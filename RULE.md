---
description: "Forbid mocks and skipped tests; require real systems"
alwaysApply: true
---

# NoMocksNoSkips Rule

Test suites must run against real implementations and must not rely on mocks or skipped tests.

Requirements:
1. Do not use mocking or stubbing frameworks, or in‑memory stand‑ins, to replace production dependencies or behaviors in tests (for example, do not mock databases, networks, filesystems, or clocks).
2. Do not skip tests due to missing dependencies or environment. If a dependency is required, provide a real test instance and configure tests to use it.
3. A passing test suite should be a credible signal that the code could be deployed on the same system/configuration used for testing.
4. If a behavior cannot be tested without mocks or skips, refactor the code or test environment so a real test is possible, or remove the behavior from this codebase’s responsibilities.
