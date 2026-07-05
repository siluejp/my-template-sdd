---
name: spec-driven-development
description: Use when defining or changing product behavior before implementation.
---

# Spec-Driven Development

## When to Use
- A feature is non-trivial, user-visible, or cross-module.
- Requirements are ambiguous.
- The implementation could expand in scope without a written boundary.

## Process
1. Identify the user problem and desired outcome.
2. Write behavior as requirements and acceptance criteria.
3. Separate goals from non-goals.
4. Capture edge cases and open questions.
5. Stop before implementation if requirements are not testable.

## Verification
- Requirements are observable.
- Acceptance criteria use concrete given/when/then or equivalent checks.
- Non-goals prevent likely scope creep.
- Open questions are explicit.

## Red Flags
- The spec describes only technical tasks.
- The agent starts coding before requirements are testable.
- Requirements include hidden implementation choices without user impact.
