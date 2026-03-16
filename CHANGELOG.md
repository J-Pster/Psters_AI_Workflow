# Changelog

All notable changes to this project will be documented in this file.

The format is inspired by Keep a Changelog.

## [0.1.3] - 2026-03-16

### Added

- Model selection guidance across planning and execution steps:
  - New section in `docs/english/workflow-methodology.md`: "Choosing the right model for each step"
  - New section in `docs/portuguese/workflow-methodology.md`: "Escolhendo o modelo certo para cada etapa"
  - New section in `README.md` (EN and PT-BR): model recommendation table per command
  - Covers rationale: planning steps (`/brainstorm`, `/plan`, `/review`) require high-capability models; execution steps (`/work-plan`, `/work`) work well with mid-tier models in auto mode

## [0.1.2] - 2026-03-16

### Added

- Maintainer release automation script:
  - `scripts/release-plugin.sh`
- Repository-level maintainer workflow helpers:
  - `.cursor/commands/develop-plugin.md`
  - `.cursor/commands/release-plugin.md`
  - `.cursor/rules/plugin-maintainer-flow.mdc`
- Claude-focused maintainer helpers:
  - `.claude/README.md`
  - `.claude/commands/develop-plugin.md`
  - `.claude/commands/release-plugin.md`
  - `.claude/agents/plugin-submission-reviewer.md`
  - `.claude/agents/plugin-release-manager.md`
- README section documenting the maintainer release flow.

## [0.1.1] - 2026-03-16

### Added

- Local manual installer script for the plugin:
  - `scripts/install-plugin-local.sh`

### Changed

- Updated getting-started docs (EN/PT) to use the installer script instead of manual copy commands.
- Refined command UX for all plugin commands by rewriting each command's first title and opening explanation for clearer discoverability and faster understanding in the command picker.
  - `/brainstorm` -> Step 1 framing
  - `/plan` -> Step 2 framing
  - `/work-plan` -> Step 3 framing
  - `/review` -> Step 4 framing
  - `/commit-changes` -> Step 5 framing
  - `/work`, `/doc`, `/compound`, `/deploy-lambda` -> concise purpose-first titles and first-line guidance

## [0.1.0] - 2026-03-16

### Added

- Initial `psters-ai-workflow` plugin structure and manifests.
- Core command set:
  - `/brainstorm`
  - `/plan`
  - `/work-plan`
  - `/work`
  - `/review`
  - `/doc`
  - `/compound`
  - `/deploy-lambda`
  - `/commit-changes`
- Rules, skills, and agents migrated and generalized for project-agnostic usage.
- Context7 MCP integration via plugin `mcp.json` and guidance rule.
- Hook automation:
  - documentation guard on session stop
  - commit convention reminder
  - migration reminder
  - code/docs edit tracking
- Bilingual documentation baseline (English and Portuguese):
  - methodology
  - commands reference
  - Extreme Programming alignment
  - getting started
  - command recipes
  - hooks reference
  - FAQ
  - add-a-plugin guide
- Contribution and community files:
  - `CONTRIBUTING.md`
  - `CODE_OF_CONDUCT.md`
  - GitHub issue and PR templates
  - Discord community link in root README
- Repository governance and release scaffolding:
  - `LICENSE` (MIT)
  - this `CHANGELOG.md`
