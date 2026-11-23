# Plugin Modular Improvement Plan

[简体中文](README.zh.md)

Open Plugins with a shortcut, reinstall local bundles, and draft audits for updates.
Each feature has its own switch.

- [Open Plugins](../dsh-plugin-panel-toggle/README.md) with `Mod+Shift+,`.
  Press it again to return to the previous page.
  `Mod` is Command on macOS and Ctrl elsewhere.
- [Reinstall a local bundle](../dsh-local-plugin-reload/README.md) from **Plugins → Local**.
  Open its details, click the pencil, then choose **Destructive reload** and confirm.
  Use the standard plugin controls to manage this aggregate itself.
- [Audit an update](../dsh-plugin-security-audit/README.md) from an installed plugin’s details
  when an update is available.
  **Audit update** opens an unsent draft in a new conversation.

## Install

Requires the Web client on DeepSeek Harness `0.2.2-rc.5` or later.

1. Run `pnpm install` in this directory.
2. If any included plugin is installed separately in this profile, note its switch state
   and remove its bundle to avoid duplicate plugin IDs.
3. In **Plugins → Add plugin**, select this directory.
   Restore any saved switch states on the new card.

[Maintenance and verification](docs/README.md)
