# Add a plugin

Add a new plugin under `plugins/` and register it in `.cursor-plugin/marketplace.json`.

## 1. Create plugin directory

Create a new folder:

```text
plugins/my-new-plugin/
```

Add the required manifest:

```text
plugins/my-new-plugin/.cursor-plugin/plugin.json
```

Example manifest:

```json
{
  "name": "my-new-plugin",
  "displayName": "My New Plugin",
  "version": "0.1.0",
  "description": "Describe what this plugin does",
  "author": {
    "name": "Your Org"
  },
  "logo": "assets/logo.svg"
}
```

## 2. Add plugin components

Add only the components you need:

- `rules/` with `.mdc` files (YAML frontmatter required)
- `skills/<skill-name>/SKILL.md` (YAML frontmatter required)
- `agents/*.md` (YAML frontmatter required)
- `commands/*.(md|mdc|markdown|txt)` (frontmatter recommended)
- `hooks/hooks.json` and `scripts/*` for automation hooks
- `mcp.json` for MCP server definitions
- `assets/logo.svg` for marketplace display

## 3. Register in marketplace manifest

Edit `.cursor-plugin/marketplace.json` and append a new entry:

```json
{
  "name": "my-new-plugin",
  "source": "./plugins/my-new-plugin",
  "description": "Describe your plugin"
}
```

`source` is the relative path from the repository root to the plugin folder.

## 4. Validate

```bash
node scripts/validate-template.mjs
```

Fix all reported errors before committing.

## 5. Common pitfalls

- Plugin `name` not kebab-case.
- `source` path in marketplace manifest does not match folder name.
- Missing `.cursor-plugin/plugin.json` in plugin folder.
- Missing frontmatter keys (`name`, `description`) in skills, agents, or commands.
- Rule files missing frontmatter `description`.
- Using a filename other than `mcp.json` for MCP server definitions.
- Broken relative paths for `logo`, `hooks`, or `mcpServers` in manifest files.
