# dsh-atlas-plugin

[简体中文](README.zh.md)

**Plugin Modular Improvement Plan.**

A modular program for differentiable, continuous improvement of the plugin management experience.
One card, one independently switchable row per enhancement.

- [Plugins panel shortcut](../dsh-plugin-panel-toggle/README.md) opens Plugins with `Mod+Shift+,` and returns
  to the previous page on the next press.
- [Local plugin reload](../dsh-local-plugin-reload/README.md) adds a Local tab.
  Open a bundle in **Plugins → Local**, click the pencil on its detail page,
  and confirm **Destructive reload** to reinstall it from source.
  Use the standard plugin controls to manage Plugin Atlas itself.
- [Plugin security audit](../dsh-plugin-security-audit/README.md) opens an unsent audit draft
  from an installed plugin's update actions.

## Install

Requires DeepSeek Harness 0.2.2-rc.5 or later with the Web client.

1. Run `pnpm install` in this directory to resolve the linked source packages.
2. If the target profile has any source bundles installed independently, record their switch states and remove them.
   Each source bundle shares its plugin row ID with the aggregate.
3. In **Plugins → Add plugin**, select this directory.
   Check the three rows and restore their switch states.

[Project documentation](docs/README.md)
