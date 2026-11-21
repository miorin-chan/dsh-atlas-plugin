# dsh-plugin-atlas

[English](README.md)

**插件模块化改良计划。**

用模块化的方式围绕插件管理体验提供可微的持续改进。
一张卡，一行一个增强，每行独立开关。

- [插件面板快捷键](../dsh-plugin-panel-toggle/README.zh.md)。
  按 `Mod+Shift+,` 打开插件页，再按一次回到刚才的页面。
- [本地插件重装](../dsh-local-plugin-reload/README.zh.md)。
  在 **插件 → 本地** 打开目标卡片，点击详情页的铅笔，再选「破坏性重装」并确认。
  本聚合卡通过插件页的常规操作管理。
- [插件安全审计](../dsh-plugin-security-audit/README.zh.md)。
  在已安装插件详情页点击「审计更新」，在新对话中预填审计草稿。

## 安装

需要 DeepSeek Harness `0.2.2-rc.5` 或更新版本及 Web 客户端。

1. 在本目录运行 `pnpm install`，链接工作区中的源插件。
2. 若目标 profile 已安装任一成员的独立 bundle，先记下开关状态并移除该 bundle。
   两种安装形式使用相同的插件行 ID。
3. 在 **插件 → 添加插件** 选择本目录，确认卡内有三行并恢复开关状态。

[项目文档](docs/README.md)
