# my-claude-plugins

A Claude Code plugin marketplace.

## Install

In Claude Code, run:

```
/plugin marketplace add krrisharora/my-claude-plugins
/plugin install starter-plugin@my-claude-plugins
```

Or add this to `~/.claude/settings.json`:

```json
{
  "extraKnownMarketplaces": {
    "my-claude-plugins": {
      "source": { "source": "github", "repo": "krrisharora/my-claude-plugins" }
    }
  },
  "enabledPlugins": {
    "starter-plugin@my-claude-plugins": true
  }
}
```

## Layout

```
.claude-plugin/marketplace.json        lists the plugins in this repo
plugins/starter-plugin/
  .claude-plugin/plugin.json           plugin name, version, author
  skills/hello/SKILL.md                an example skill
```

## Adding a skill

1. Make a folder `plugins/starter-plugin/skills/<skill-name>/`.
2. Put a `SKILL.md` in it (copy `hello` as a template).
3. Bump `version` in both `plugin.json` and `marketplace.json`, then commit and push.
