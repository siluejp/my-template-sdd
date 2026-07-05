# SDD Workflow

This template combines GitHub Spec Kit command skills with focused supplementary
agent skills.

## Setup

Install the Specify CLI using the current instructions from GitHub Spec Kit, then initialize the project for your agent.

```sh
specify init . --integration codex --integration-options="--skills"
```

This repository is initialized for Codex skills mode, so Spec Kit commands are
available as `.agents/skills/speckit-*`.

## Feature Flow

1. Update project principles with `$speckit-constitution` when the development rules change.
2. Create a feature spec with `$speckit-specify`.
3. Resolve ambiguity with `$speckit-clarify`.
4. Create the implementation plan with `$speckit-plan`.
5. Break the plan into tasks with `$speckit-tasks`.
6. Run `$speckit-analyze` before implementation.
7. Implement with `$speckit-implement`.
8. Run `$speckit-converge` to find drift between artifacts and code.

## Skill Usage

Load only the supplementary skill needed for the current phase. These skills
guide behavior but do not replace the Spec Kit command skills in `.agents/skills/`.

- `skills/spec-driven-development/SKILL.md`: requirements and acceptance criteria
- `skills/planning-and-task-breakdown/SKILL.md`: technical plan and tasks
- `skills/test-driven-development/SKILL.md`: implementation and regression checks
- `skills/code-review-and-quality/SKILL.md`: final review
- `skills/security-and-hardening/SKILL.md`: security-sensitive work

## Artifact Rules

- Keep feature artifacts under `specs/<number>-<kebab-name>/`.
- Keep specs current while work is in progress.
- If implementation scope changes, update the spec or plan before continuing.
- Do not put credentials, personal data, or production secrets in specs.
