# GitHub Wiki Sync

This project can publish the `docs/` content into the repository Wiki.

## One-time GitHub UI setup

1. Open repository `Settings`.
2. In `Features`, enable `Wikis`.
3. Go to `Actions` tab.
4. Run workflow **Sync Docs to Wiki** manually once.

## Ongoing behavior

- Every push to `main` that changes docs triggers sync automatically.
- The workflow exports docs pages and updates the Wiki repo.

## Special page for marketing audiences

- The page `docs/english/marketing-workflows.md` is included in wiki sync.
- It acts as a bridge for users asking for a marketing-focused workflow path.

## If sync fails

- Confirm Wiki is enabled.
- Confirm Actions are enabled for the repository.
- Re-run workflow from `Actions` tab.
