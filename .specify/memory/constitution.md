# My Template SDD Constitution

## Core Principles

### I. Spec as Source of Truth
Every non-trivial feature MUST start from a written specification. Implementation
decisions MUST trace back to `spec.md`, `plan.md`, and `tasks.md` under the active
`specs/<number>-<kebab-name>/` directory.

### II. Testable Outcomes
Requirements MUST be stated as observable behavior. Each important requirement
MUST have an acceptance scenario, automated test, or explicit manual verification
step before implementation is considered complete.

### III. Minimal Context Loading
Agents SHOULD load only the Spec Kit command skill and supplementary workflow
skill needed for the current phase. Large unrelated context SHOULD be avoided so
the active spec, plan, tasks, and repository evidence stay prominent.

### IV. Human-Readable Decisions
Tradeoffs, rejected approaches, assumptions, and open questions MUST be recorded
in the feature artifacts. Future agents and reviewers must be able to recover the
reasoning without relying on conversation history.

### V. Security and Privacy by Default
Secrets, personal data, and production credentials MUST NOT be written into specs,
examples, logs, or documentation. Security-sensitive work MUST include explicit
review of authorization, data exposure, logging, and failure behavior.

## Additional Constraints

- GitHub Spec Kit core templates are the default artifact structure.
- Project-local template overrides are allowed only when they preserve the
  sections required by the installed Spec Kit command skills.
- Supplementary skills under `skills/` provide phase guidance; they do not replace
  `.agents/skills/speckit-*` command skills.
- Feature artifacts live under `specs/<number>-<kebab-name>/`.

## Development Workflow

1. Use `$speckit-constitution` when changing project principles.
2. Use `$speckit-specify` to create or update requirements.
3. Use `$speckit-clarify` when requirements remain ambiguous.
4. Use `$speckit-plan` to produce technical design artifacts.
5. Use `$speckit-tasks` to generate implementation tasks.
6. Use `$speckit-analyze` before implementation to check artifact consistency.
7. Use `$speckit-implement` to execute the task list.
8. Use `$speckit-converge` to find and close spec-code drift.

## Governance

This constitution supersedes ad hoc workflow preferences for this template.
Amendments MUST update this file and any affected guidance in `AGENTS.md`,
`README.md`, or `docs/`. Version changes follow semantic versioning: MAJOR for
incompatible governance changes, MINOR for new principles or required workflow
steps, and PATCH for wording-only clarifications. Reviews MUST check that active
feature artifacts comply with these principles before completion.

**Version**: 1.0.0 | **Ratified**: 2026-07-05 | **Last Amended**: 2026-07-05
