# 插件模块化改良计划

[English](README.md)

用快捷键打开插件页、重装本地插件，或为插件更新起草审计。
三项功能可独立开关。

- [打开插件页](../dsh-plugin-panel-toggle/README.zh.md)。
  按 `Mod+Shift+,` 打开，再按一次返回上一页。
  macOS 的 `Mod` 是 Command，其他平台是 Ctrl。
- [重装本地插件](../dsh-local-plugin-reload/README.zh.md)。
  在 **插件 → 本地** 打开目标详情，点铅笔，选择 **破坏性重装** 并确认。
  本聚合包本身通过插件页的常规操作管理。
- [审计插件更新](../dsh-plugin-security-audit/README.zh.md)。
  在有可用更新的已安装插件详情中，点 **审计更新**，在新对话中打开待发送的审计草稿。

## 安装

需要 DeepSeek Harness `0.2.2-rc.5` 或更新版本的 Web 客户端。

1. 在本目录运行 `pnpm install`。
2. 如果当前 profile 已单独安装其中的插件，先记下开关状态，再移除独立安装的包，避免插件 ID 重复。
3. 在 **插件 → 添加插件** 选择本目录，再到新卡片恢复已记下的开关状态。

[维护与验证](docs/README.md)
