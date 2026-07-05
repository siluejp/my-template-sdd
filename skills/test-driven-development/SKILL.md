---
name: test-driven-development
description: Use when implementing code that needs reliable behavior and regression coverage.
---

# Test-Driven Development

## When to Use
- Writing or changing production code.
- Fixing a bug.
- Implementing acceptance criteria from a spec.

## Process
1. Identify the behavior to prove.
2. Add a failing test or define a concrete manual check if automated testing is unavailable.
3. Implement the smallest change that passes.
4. Refactor only after verification passes.
5. Run the relevant test/check before completion.

## Verification
- At least one test or check maps to each important requirement.
- Regression behavior is covered for bug fixes.
- The final answer states what was run and any gaps.

## Red Flags
- Tests are added only after implementation without proving they fail.
- Manual verification is vague.
- Unrelated refactors are mixed into the change.
