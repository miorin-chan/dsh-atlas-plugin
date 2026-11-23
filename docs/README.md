# 项目文档

## 使用

- [打开插件页](../../dsh-plugin-panel-toggle/README.zh.md)。
  按 `Mod+Shift+,` 打开，再按一次返回上一页。
  macOS 的 `Mod` 是 Command，其他平台是 Ctrl。
- [重装本地插件](../../dsh-local-plugin-reload/README.zh.md)。
  在 **插件 → 本地** 打开目标详情，点铅笔，选择 **破坏性重装** 并确认。
  本聚合包本身通过插件页的常规操作管理。
- [审计插件更新](../../dsh-plugin-security-audit/README.zh.md)。
  在有可用更新的已安装插件详情中，点 **审计更新**，在新对话中打开待发送的审计草稿。

## 兼容条件

需要 DeepSeek Harness `0.2.2-rc.5` 或更新版本的 Web 客户端。

## 安装

1. 在聚合包目录运行 `pnpm install`。
2. 如果目标 profile 已单独安装任何成员，记下开关状态，再移除独立安装的包，避免行 ID 重复。
3. 在 **插件 → 添加插件** 选择聚合包目录，然后在新卡片恢复各成员的开关状态。

[聚合清单](../aggregate.yml)声明卡内成员和顺序。生成器保留原行 ID 和配置。
在包目录用 `pnpm run aggregate` 更新生成物，随后运行 `pnpm install` 与 `pnpm run check`。

本地重装通过 bundle 的成员行识别承载自己的卡片。
该卡片仍可浏览并可用常规开关管理，重装工具只处理其他本地 bundle。

## 验证

一次性 profile 中确认三个源插件可独立启停，关闭整卡后撤下三行，恢复后各出现一次。
浏览器中检查快捷键双向切换与「本地」标签页。
审计入口的行为与范围见[审计插件文档](../../dsh-plugin-security-audit/docs/README.md)。
聚合卡详情应隐藏其自身的重装入口，其他可移除的本地 bundle 仍可使用重装入口。

2026-11-21 在 DSH `0.2.2-rc.5` 上使用一次性 Web profile 验证。
合成配置中每个成员各出现一次，两个行开关可独立覆盖，整包移除和恢复同时撤下和恢复两行。
快捷键和重装的源插件测试均通过。通过 Chrome 打开「插件 → 本地 → Plugin Modular Improvement Plan」，
确认两条成员行可见，聚合卡没有自身的重装入口，浏览器没有报错。
浏览器冒烟覆盖卡片和自我保护；快捷键双向切换与其他 bundle 的重装由源插件测试覆盖。

同日在一次性 profile 中安装三成员聚合包，以本地注册表提供 `1.0.0 → 2.0.0` 更新夹具。
Chrome 中确认审计按钮在原生更新旁，点击后只有输入框显示版本审计提示词，会话记录没有对应消息。
停用审计成员后，审计按钮消失，原生更新仍可用，其他两项保持启用。

## Usage

- [Open Plugins](../../dsh-plugin-panel-toggle/README.md) with `Mod+Shift+,`.
  Press it again to return to the previous page.
  `Mod` is Command on macOS and Ctrl elsewhere.
- [Reinstall a local bundle](../../dsh-local-plugin-reload/README.md) from **Plugins → Local**.
  Open its details, click the pencil, then choose **Destructive reload** and confirm.
  Use the standard plugin controls to manage this aggregate itself.
- [Audit an update](../../dsh-plugin-security-audit/README.md) from an installed plugin’s details
  when an update is available.
  **Audit update** opens an unsent draft in a new conversation.

## Compatibility

Requires the Web client on DeepSeek Harness `0.2.2-rc.5` or later.

## Install

1. Run `pnpm install` from the bundle directory.
2. If any member is installed separately in the target profile, note its switch state and remove its bundle
   to avoid duplicate row IDs.
3. In **Plugins → Add plugin**, select the bundle directory.
   Restore the saved switch states on the new card.
