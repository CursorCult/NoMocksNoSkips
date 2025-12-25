# ⚠️ DEPRECATED

This rule has been replaced by [PAPER](https://github.com/CursorCult/PAPER).

PAPER ("Paper-thin Assertions Pathetically Exercising Reality") cleanly subsumes this rule by focusing on behavioral reality rather than implementation details.

---

# NoMocksNoSkips

Forbid mocks and skipped tests; require real systems.

**Install**

```sh
pipx install cursorcult
cursorcult link NoMocksNoSkips
```

Rule file format reference: https://cursor.com/docs/context/rules#rulemd-file-format

**When to use**

- You want passing tests to mean “this could run in the real world.”
- You’re debugging failures that only appear outside mocked environments.
- Your project can afford real test dependencies (databases, services, etc.).

**What it enforces**

- Tests avoid mocks/stubs for production dependencies.
- Tests are not skipped because a dependency is missing; provide it.
- A green suite implies deployable behavior on that system.

**Credits**

- Developed by Will Wieselquist. Anyone can use it.