# psters-ai-workflow

Daily AI development workflow plugin for Cursor.

## Installation

This plugin is registered in `.cursor-plugin/marketplace.json` for this repository.

To validate submission readiness:

`node scripts/validate-template.mjs`

## Included

- `rules/`: commit conventions, markdown discipline, and doc-first library usage
- `skills/`: commit orchestration, per-repo commit worker, NestJS/Angular conventions, Lambda deploy, git-worktree
- `agents/`: full workflow agents — review (simplicity, security, architecture, schema-drift, performance, etc.), design, docs, research, workflow
- `commands/`: `brainstorm`, `plan`, `work-plan`, `work`, `review`, `doc`, `compound`, `deploy-lambda`, `commit-changes`

This plugin includes all agents and skills from the complete AI workflow.

## Context7 MCP

This plugin includes `mcp.json` with a Context7 MCP server setup.

- Server key: `context7`
- Required flow: `resolve-library-id` -> `query-docs`
- Guidance rule: `rules/context7-documentation.mdc`

Use this flow whenever implementation depends on external library/framework docs.

## Workflow

`/brainstorm` -> `/plan` -> `/work-plan` (or `/work`) -> `/review` -> `/commit-changes`

## Usage Notes

- Keep commits focused and ticket-aware when possible.
- Use `/plan` for multi-step changes.
- Use `/work` for direct implementation requests.
- Use `/review` before opening a pull request.
