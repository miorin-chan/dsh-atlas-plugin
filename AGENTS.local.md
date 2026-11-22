# AGENTS.local

`aggregate.yml` 声明成员与顺序。使用 `pnpm run aggregate` 生成依赖和 patch，保留源插件行 ID 与配置。
行为改动留在源插件中。成员变动后运行 `pnpm install`、`pnpm run check` 与工作区的插件骨架校验。
安装验证使用一次性 profile。

[英文用户说明](README.md)、[中文用户说明](README.zh.md)和[项目文档](docs/README.md)分别保存安装说明与验证记录。
卡片元数据同时维护八个 locale。Markdown 使用 `docs/scripts/reflow md`，Git 钩子通过 `prek install` 安装。

## 复用 DSH 原生界面

- 优先复用 DSH 原生组件、行为、主题 token 和同类界面布局，以减少自写代码和维护成本。
- 当前版本有受支持的运行时入口且性能可接受时，优先通过公开插槽、
  组件工厂或宿主提供的可加载模块动态复用，让宿主提供组件实现。
  只有现有组件和扩展点无法满足需求时，才补足必要的插件实现。
- 静态引入或打包官方代码或资源时，在引用处标注上游包名、版本或提交、源码路径及符号名，便于升级时回看和同步，
  并保留适用的许可证与署名。
