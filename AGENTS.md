# Repository Guidelines

## Project Structure & Module Organization
- `README.md`: このテンプレートの概要と導入手順。
- `AGENTS.md`: AI coding agent 共通の作業ルール。
- `.specify/`: GitHub Spec Kit の原則、core テンプレート、スクリプト。
- `.agents/skills/`: Spec Kit が生成する Codex skills mode 用の実行スキル。
- `specs/`: 機能ごとの SDD 成果物。`spec.md`、`plan.md`、`tasks.md` を配置します。
- `skills/`: 補助的な agent-skills 形式の工程別 `SKILL.md`。Spec Kit 実行スキルは置き換えません。
- `docs/`: ワークフローや運用メモ。
- `.devcontainer/`: 開発コンテナ設定。

## Build, Test, and Development Commands
- このリポジトリは SDD テンプレートのため、固定のビルド・テストコマンドはありません。
- 構成確認: `rg --files`
- Spec Kit の初期化例: `specify init . --integration codex --integration-options="--skills"`
- Spec Kit の利用可能統合確認: `specify integration list`

## SDD Workflow
非自明な機能追加・仕様変更では、GitHub Spec Kit の成果物を共有ソースとして扱います。

1. 原則を定義または更新する: `$speckit-constitution`
2. 要件を定義する: `$speckit-specify`
3. 不明点を解消する: `$speckit-clarify`
4. 技術計画を作る: `$speckit-plan`
5. 実装タスクへ分解する: `$speckit-tasks`
6. 成果物間の整合性を確認する: `$speckit-analyze`
7. 実装する: `$speckit-implement`
8. 仕様・計画・タスクと実装の差分を収束させる: `$speckit-converge`

このリポジトリは Codex skills mode で初期化されているため、Spec Kit の実行スキルは
`.agents/skills/speckit-*/SKILL.md` を使います。

## Skill Loading Policy
常時すべてのスキルを読み込まず、作業フェーズに必要なものだけを使います。Spec Kit
コマンドは `.agents/skills/`、補助プロセスは `skills/` を参照します。

- 要件定義: `skills/spec-driven-development/SKILL.md`
- 技術計画: `skills/planning-and-task-breakdown/SKILL.md`
- 実装: `skills/test-driven-development/SKILL.md`
- 完了前レビュー: `skills/code-review-and-quality/SKILL.md`
- セキュリティ影響あり: `skills/security-and-hardening/SKILL.md`

## Coding Style & Naming Conventions
- Markdown は見出しと箇条書きを簡潔に保ちます。
- Spec Kit 成果物は `specs/<number>-<kebab-name>/` に置きます。
- Spec Kit core テンプレートを標準とします。上書きが必要な場合は、core が要求する必須セクションを維持します。

## Testing Guidelines
- 実装リポジトリへ展開した後は、そのリポジトリの標準テストを使います。
- テストコマンドが未定義の場合、`tasks.md` に検証方法を明記します。
- 実装タスクには、失敗するテストまたは検証手順を先に置きます。

## Commit & Pull Request Guidelines
- PR には対応する `specs/<number>-<name>/` を記載します。
- 仕様変更を伴う実装では、コードだけでなく `spec.md`、`plan.md`、`tasks.md` の更新も確認します。
- 完了前にレビュー用スキルを使い、未解決リスクを PR に残します。

## Security & Configuration Tips
- `.env`、認証情報、個人ログをコミットしません。
- `specs/` や `docs/` に個人情報、秘密情報、本番トークンを記載しません。
- セキュリティ、権限、データ保持、外部連携に触れる変更は `security-and-hardening` を適用します。
