# Bagrat's Claude Code plugins

A [Claude Code plugin marketplace](https://code.claude.com/docs/en/plugin-marketplaces).
Add it once; install any plugin listed here, and get new ones automatically as they ship.

```
/plugin marketplace add bagrat/claude-plugins
/plugin install shroom
```

## Plugins

| Plugin | What it does |
| --- | --- |
| [**shroom**](https://github.com/bagrat/shroom) | Agent-first, self-hosted Loom alternative — record your screen to your own object storage + git and get a permanent unlisted link with auto title, chapters, and a searchable transcript. |

## How this is wired

This repo is a **thin catalog** — it holds only `marketplace.json`. Each plugin lives in
its **own** repository (e.g. `bagrat/shroom`) and is referenced by a `github` source. That
means:

- **Each plugin versions itself.** A plugin's version comes from its own `plugin.json`;
  users get an update when that version string changes. Releasing a plugin does **not**
  require a commit here.
- **This catalog only changes when the lineup does** — i.e. when a new plugin is added.
- Users add **one** marketplace, ever, and pick up new plugins as they appear.
