# AGENTS.local

`aggregate.yml` 声明成员与顺序。使用 `pnpm run aggregate` 生成依赖和 patch，保留源插件行 ID 与配置。
行为改动留在源插件中。成员变动后运行 `pnpm install`、`pnpm run check` 与工作区的插件骨架校验。
安装验证使用一次性 profile。

[英文用户说明](README.md)、[中文用户说明](README.zh.md)和[项目文档](docs/README.md)分别保存安装说明与验证记录。
卡片元数据同时维护八个 locale。Markdown 使用 `docs/scripts/reflow md`，Git 钩子通过 `prek install` 安装。
