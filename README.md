# my-template-sdd

Template for Spec-Driven Development with GitHub Spec Kit and focused agent skills.

## What This Provides

- GitHub Spec Kit project memory, core templates, and scripts under `.specify/`
- Agent-readable workflow rules in `AGENTS.md`
- Spec Kit command skills under `.agents/skills/`
- Supplementary phase skills under `skills/`
- A short operating guide in `docs/workflow.md`

## Recommended Flow

1. Define project principles with `$speckit-constitution`.
2. Write requirements with `$speckit-specify`.
3. Clarify ambiguity with `$speckit-clarify`.
4. Create the technical plan with `$speckit-plan`.
5. Generate implementation tasks with `$speckit-tasks`.
6. Validate artifact consistency with `$speckit-analyze`.
7. Implement with `$speckit-implement`.
8. Reconcile drift with `$speckit-converge`.

## Skill Policy

Load supplementary skills selectively. Spec Kit execution itself uses
`.agents/skills/speckit-*`.

- Requirements: `skills/spec-driven-development/SKILL.md`
- Planning: `skills/planning-and-task-breakdown/SKILL.md`
- Implementation: `skills/test-driven-development/SKILL.md`
- Review: `skills/code-review-and-quality/SKILL.md`
- Security-sensitive work: `skills/security-and-hardening/SKILL.md`

See `docs/workflow.md` for the full workflow.
