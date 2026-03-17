# Sincronizacao com GitHub Wiki

Este projeto pode publicar o conteudo de `docs/` na Wiki do repositorio.

## Setup unico na UI do GitHub

1. Abra `Settings` do repositorio.
2. Em `Features`, ative `Wikis`.
3. Abra a aba `Actions`.
4. Execute manualmente o workflow **Sync Docs to Wiki** uma vez.

## Comportamento continuo

- Todo push em `main` que altere docs dispara sincronizacao automatica.
- O workflow exporta as paginas de docs e atualiza o repositorio da Wiki.

## Pagina especial para audiencia de marketing

- A pagina `docs/portuguese/marketing-workflows.md` e incluida na sincronizacao.
- Ela serve como ponte para quem pergunta por um workflow focado em marketing.

## Se falhar

- Confirme que a Wiki esta ativada.
- Confirme que Actions estao habilitadas no repositorio.
- Rode o workflow novamente pela aba `Actions`.
