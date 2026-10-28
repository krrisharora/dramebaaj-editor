# Dramebaaj Editor

A Claude Code plugin marketplace.

## Install

In Claude Code, run:

```
/plugin marketplace add krrisharora/dramebaaj-editor
/plugin install dramebaaj-editor@dramebaaj-editor
```

Or add this to `~/.claude/settings.json`:

```json
{
  "extraKnownMarketplaces": {
    "dramebaaj-editor": {
      "source": { "source": "github", "repo": "krrisharora/dramebaaj-editor" }
    }
  },
  "enabledPlugins": {
    "dramebaaj-editor@dramebaaj-editor": true
  }
}
```

## Layout

```
.claude-plugin/marketplace.json        lists the plugins in this repo
plugins/dramebaaj-editor/
  .claude-plugin/plugin.json           plugin name, version, author
  skills/hello/SKILL.md                an example skill
```

## Adding a skill

1. Make a folder `plugins/dramebaaj-editor/skills/<skill-name>/`.
2. Put a `SKILL.md` in it (copy `hello` as a template).
3. Bump `version` in both `plugin.json` and `marketplace.json`, then commit and push.
