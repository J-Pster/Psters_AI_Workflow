# psters-ai-workflow

An anti-vibe-coding, agentic AI workflow plugin for any project, language, and framework, with structured planning, phased execution, review, and continuous documentation.

![psters-ai-workflow logo](assets/logo.svg)

![Plugin](https://img.shields.io/badge/cursor-plugin-green) ![Docs](https://img.shields.io/badge/docs-bilingual-blue) ![MCP](https://img.shields.io/badge/MCP-Context7-6f42c1) ![Hooks](https://img.shields.io/badge/hooks-enabled-orange)

## Language

- English: [jump to English section](#plugin-explained-english)
- Portuguese (PT-BR): [jump to Portuguese section](#plugin-explicado-portugues-pt-br)

## Documentation links

- Docs index (start here): [../../docs/README.md](../../docs/README.md)
- English docs index: [../../docs/english/README.md](../../docs/english/README.md)
- Portuguese docs index: [../../docs/portuguese/README.md](../../docs/portuguese/README.md)
- Contribution guide: [../../CONTRIBUTING.md](../../CONTRIBUTING.md)

### English docs

- [Getting started](../../docs/english/getting-started.md)
- [Workflow methodology](../../docs/english/workflow-methodology.md)
- [Commands reference](../../docs/english/commands-reference.md)
- [Command recipes](../../docs/english/command-recipes.md)
- [Examples in practice](../../docs/english/examples-in-practice.md)
- [Hooks reference](../../docs/english/hooks-reference.md)
- [FAQ](../../docs/english/faq.md)
- [Docs quality checklist](../../docs/english/docs-quality-checklist.md)
- [Wiki sync](../../docs/english/wiki-sync.md)

### Portuguese docs

- [Comece em 10 minutos](../../docs/portuguese/getting-started.md)
- [Metodologia do workflow](../../docs/portuguese/workflow-methodology.md)
- [Referencia de comandos](../../docs/portuguese/commands-reference.md)
- [Receitas de comandos](../../docs/portuguese/command-recipes.md)
- [Exemplos na pratica](../../docs/portuguese/examples-in-practice.md)
- [Referencia de hooks](../../docs/portuguese/hooks-reference.md)
- [FAQ](../../docs/portuguese/faq.md)
- [Checklist de qualidade de documentacao](../../docs/portuguese/docs-quality-checklist.md)
- [Sincronizacao com wiki](../../docs/portuguese/wiki-sync.md)

## Quick map

- [Plugin Overview (English)](#plugin-overview-english)
- [Workflow](#workflow)
- [`/doc` vs `/compound`](#doc-vs-compound)
- [Hooks Automation](#hooks-automation)
- [Context7 MCP](#context7-mcp)

---

<a id="plugin-explained-english"></a>

## Plugin Overview (English)

Daily AI development workflow plugin for Cursor. **Anti-vibe-coding** by design.

### Installation

### Marketplace

When published, install from [Cursor Marketplace](https://cursor.com/marketplace).

### Manual install

1. Run:
   - `./scripts/install-plugin-local.sh`
2. Restart Cursor (or reload window) to activate the plugin.

This plugin is also registered in `.cursor-plugin/marketplace.json` for this repository.

To validate submission readiness:

`node scripts/validate-template.mjs`

### Included

- **rules/**: commit conventions, markdown discipline, TypeORM migrations, Context7 documentation
- **skills/**: commit orchestration, per-repo commit worker, NestJS/Angular conventions, Lambda deploy, git-worktree
- **agents/**: full workflow agents — review (simplicity, security, architecture, schema-drift, performance, etc.), design, docs, research, workflow
- **commands/**: `brainstorm`, `plan`, `work-plan`, `work`, `review`, `doc`, `compound`, `deploy-lambda`, `commit-changes`

### Anti-vibe coding

This plugin enforces:

- **Contextualization**: `/work` and `/work-plan` read docs first, never jump to implementation.
- **Documentation**: Both commands update docs as part of their mandatory workflow (doc-shepherd, module/feature/lambda docs).
- **Structure**: Phases, tasks, review loops, and commit conventions keep work traceable.

### Workflow

`/brainstorm` -> `/plan` -> `/work-plan` (or `/work`) -> `/review` -> `/commit-changes`

### `/doc` vs `/compound`

- `/work` and `/work-plan` already update docs as part of their mandatory execution flow.
- `/doc`: explicitly force canonical system documentation generation/update (module, feature, architecture, ADR, full update).
- `/compound`: explicitly force learning documentation (problem/solution writeups and reusable implementation patterns).

Use `/doc` for "how the system is structured now" and `/compound` for "what we learned and should reuse".

> Important: `/doc` and `/compound` complement `/work` and `/work-plan`; they do not replace them.

### Hooks Automation

This plugin includes workflow hooks in `hooks/hooks.json` to reinforce anti-vibe-coding behavior:

- `afterFileEdit` -> tracks whether the session changed code and/or docs.
- `stop` -> reminds to run `/doc update` (and `/compound` when relevant) if code changed without documentation updates.
- `beforeShellExecution` (matcher: `git commit`) -> reminds commit message convention (`[TICKET-XXXX] ...`).
- `afterShellExecution` (matcher: `typeorm:generate`) -> reminds the migration atomic chain.

### Usage Notes

- Keep commits focused and ticket-aware when possible.
- Use `/plan` for multi-step changes.
- Use `/work` for direct implementation requests.
- Use `/review` before opening a pull request.
- **Never skip documentation** — `/work` and `/work-plan` update docs as part of the flow.

### Context7 MCP

This plugin includes `mcp.json` with a Context7 MCP server setup.

- Server key: `context7`
- Required flow: `resolve-library-id` -> `query-docs`
- Guidance rule: `rules/context7-documentation.mdc`

Use this flow whenever implementation depends on external library/framework docs.

---

<a id="plugin-explicado-portugues-pt-br"></a>

## Visão Geral do Plugin (Português - PT-BR)

Plugin de workflow diario de IA para Cursor. **Anti-vibe-coding** por design.

### Instalacao

### Marketplace

Quando publicado, instale via [Cursor Marketplace](https://cursor.com/marketplace).

### Instalacao manual

1. Rode:
   - `./scripts/install-plugin-local.sh`
2. Reinicie o Cursor (ou recarregue a janela) para ativar.

Este plugin tambem esta registrado em `.cursor-plugin/marketplace.json` neste repositorio.

Para validar prontidao de submissao:

`node scripts/validate-template.mjs`

### O que esta incluido

- **rules/**: convencoes de commit, disciplina de markdown, migrations TypeORM, documentacao Context7, texto para usuario, AWS CLI
- **skills/**: orquestracao de commits, worker por repositorio, convencoes NestJS/Angular, deploy de Lambda, git-worktree
- **agents/**: suite completa de agentes — review (simplicidade, seguranca, arquitetura, schema-drift, performance etc.), design, docs, research, workflow
- **commands/**: `brainstorm`, `plan`, `work-plan`, `work`, `review`, `doc`, `compound`, `deploy-lambda`, `commit-changes`

### Anti-vibe coding

Este plugin reforca:

- **Contextualizacao**: `/work` e `/work-plan` leem docs primeiro, sem pular direto para implementacao.
- **Documentacao**: ambos os comandos atualizam docs como parte obrigatoria do fluxo (doc-shepherd, docs de modulo/feature/lambda).
- **Estrutura**: fases, tarefas, loops de review e convencoes de commit mantem rastreabilidade.

### Workflow

`/brainstorm` -> `/plan` -> `/work-plan` (ou `/work`) -> `/review` -> `/commit-changes`

### `/doc` vs `/compound`

- `/work` e `/work-plan` ja atualizam docs como parte obrigatoria do fluxo de execucao.
- `/doc`: forca explicitamente geracao/atualizacao da documentacao canonica do sistema (modulo, feature, arquitetura, ADR, update geral).
- `/compound`: forca explicitamente documentacao de aprendizado (problema/solucao e padroes reutilizaveis).

Use `/doc` para "como o sistema esta agora" e `/compound` para "o que aprendemos e devemos reaproveitar".

> Importante: `/doc` e `/compound` complementam `/work` e `/work-plan`; nao substituem esses comandos.

### Automacao com Hooks

Este plugin inclui hooks em `hooks/hooks.json` para reforcar anti-vibe-coding:

- `afterFileEdit` -> rastreia se a sessao alterou codigo e/ou docs.
- `stop` -> lembra de rodar `/doc update` (e `/compound`, quando fizer sentido) se houve mudanca de codigo sem atualizar docs.
- `beforeShellExecution` (matcher: `git commit`) -> lembra convencao de commit (`[TICKET-XXXX] ...`).
- `afterShellExecution` (matcher: `typeorm:generate`) -> lembra cadeia atomica de migrations.

### Notas de uso

- Mantenha commits focados e, quando possivel, vinculados a ticket.
- Use `/plan` para mudancas multi-etapas.
- Use `/work` para implementacoes diretas.
- Use `/review` antes de abrir PR.
- **Nao pule documentacao** — `/work` e `/work-plan` atualizam docs como parte do fluxo.

### Context7 MCP

Este plugin inclui `mcp.json` com configuracao do servidor Context7 MCP.

- Chave do servidor: `context7`
- Fluxo obrigatorio: `resolve-library-id` -> `query-docs`
- Regra de referencia: `rules/context7-documentation.mdc`

Use esse fluxo sempre que a implementacao depender de docs de bibliotecas/frameworks externos.
