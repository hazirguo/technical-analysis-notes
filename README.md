# technical-analysis-notes

专门存放我与 Muse 协作完成的技术分析产物的公开仓库：交互式架构图、源码分析与深度拆解。所有网页产物通过 GitHub Pages 发布，可直接在线浏览。

在线浏览：https://hazirguo.github.io/technical-analysis-notes/

## 产物列表

| 日期 | 产物 | 说明 | 链接 |
|---|---|---|---|
| 2026-10-26 | Muse 平台技术架构图 | 六层分层总览、一次请求的 7 步生命周期、Agent 协作拓扑、记忆系统、安全与信任边界、核心组件速览；可点击交互 | [在线浏览](https://hazirguo.github.io/technical-analysis-notes/muse-architecture/) · [源码目录](./muse-architecture/) |

## 目录约定

- 每个产物一个顶层目录，目录名用 kebab-case，例如 `muse-architecture/`
- 产物入口统一为该目录下的 `index.html`（自包含单文件优先，避免资源依赖失效）
- 新增产物后，同步更新本表与根目录 `index.html` 索引页

## 发布方式

GitHub Pages 已开启，来源为 `main` 分支根目录：推送到 `main` 后 Pages 会自动重新构建发布，无需其他操作。
