---
name: code-review-and-quality
description: Use before completing a change to check correctness, maintainability, and drift from the spec.
---

# Code Review and Quality

## When to Use
- Before handing off a completed implementation.
- When reviewing a branch or pull request.
- After Spec Kit implementation to find drift from `spec.md`, `plan.md`, and `tasks.md`.

## Process
1. Compare implementation against requirements and tasks.
2. Look for correctness bugs, edge cases, regressions, and missing tests.
3. Check maintainability, naming, boundaries, and unnecessary complexity.
4. Verify commands actually run or record why they could not.
5. List findings by severity with file and line references.

## Verification
- No known requirement is unimplemented without a documented reason.
- Tests/checks cover the changed behavior.
- Remaining risks are explicit.

## Red Flags
- Review focuses on style while missing behavior.
- The agent says "looks good" without evidence.
- Spec, plan, tasks, and code disagree.
