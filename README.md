# Bagrat's Claude Code plugins

A [Claude Code plugin marketplace](https://code.claude.com/docs/en/plugin-marketplaces).
Add it once; install any plugin listed here, and get new ones automatically as they ship.

```
/plugin marketplace add bagrat/claude-plugins
```

## Plugins

None listed right now. shroom used to live here as a plugin; it is now a Mac app — see
[shroom.am](https://shroom.am).

## How this is wired

This repo is a **thin catalog** — it holds only `marketplace.json`. Each plugin lives in
its **own** repository and is referenced by a `github` source. That
means:

- **Each plugin versions itself.** A plugin's version comes from its own `plugin.json`;
  users get an update when that version string changes. Releasing a plugin does **not**
  require a commit here.
- **This catalog only changes when the lineup does** — i.e. when a new plugin is added.
- Users add **one** marketplace, ever, and pick up new plugins as they appear.
