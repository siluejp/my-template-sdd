---
name: planning-and-task-breakdown
description: Use when turning a spec into technical design and implementation tasks.
---

# Planning and Task Breakdown

## When to Use
- A completed spec needs a technical path.
- Multiple files, modules, or systems are affected.
- Work needs ordering before implementation.

## Process
1. Read the spec and existing code patterns first.
2. Choose the smallest architecture that satisfies the requirements.
3. Record dependencies, interfaces, risks, and test strategy.
4. Break work into independently verifiable tasks.
5. Put tests and checks before implementation tasks where practical.

## Verification
- Each task has a clear output.
- The plan names affected boundaries and integration points.
- Risks have mitigations or follow-up tasks.
- The task list can be executed without re-planning.

## Red Flags
- Tasks are broad phases like "build backend" without concrete outputs.
- The plan invents a new architecture without checking existing patterns.
- Verification is deferred until after all implementation.
