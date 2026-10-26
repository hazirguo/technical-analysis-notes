# technical-analysis-notes

专门存放我与 Muse 协作完成的技术分析产物的公开仓库：交互式架构图、源码分析与深度拆解。所有网页产物通过 GitHub Pages 发布，可直接在线浏览。

在线浏览：https://hazirguo.github.io/technical-analysis-notes/

## 产物列表

| 日期 | 产物 | 说明 | 链接 |
|---|---|---|---|
| 2026-10-26 | Muse 平台技术架构图 | 六层分层总览、一次请求的 7 步生命周期、Agent 协作拓扑、记忆系统、安全与信任边界、核心组件速览；可点击交互 | [在线浏览](https://hazirguo.github.io/technical-analysis-notes/muse-architecture/) · [源码目录](./muse-architecture/) |
| 2026-10-22 | vhost-xx 设备原理与场景 | 8 章：纯 virtio 三笔税、四种后端（纯 QEMU / vhost-net / vhost-user+DPDK / vDPA）数据面路径实验室、virtqueue 三环演示、7 步建立流程、9 个家族成员图鉴、拷贝次数对比、6 个应用场景、两问选型速判 | [在线浏览](https://hazirguo.github.io/technical-analysis-notes/vhost-xx/) · [源码目录](./vhost-xx/) |
| 2026-10-20 | Escaping SPACE 红队报告 · 中文汇报 | Perplexity 红队报告（2026-09-23）中文汇报：9 个前沿模型 108 次 VM 逃逸 0 成功、两种 egress 绕过手法（DNS 欺骗 / IP 共享 domain fronting）、修复与复测、10 家第三方沙箱横测与厂商响应、沙箱建设者检查清单 | [在线浏览](https://hazirguo.github.io/technical-analysis-notes/escaping-space/) · [源码目录](./escaping-space/) |

## 目录约定

- 每个产物一个顶层目录，目录名用 kebab-case，例如 `muse-architecture/`
- 产物入口统一为该目录下的 `index.html`（自包含单文件优先，避免资源依赖失效）
- 新增产物后，同步更新本表与根目录 `index.html` 索引页

## 发布方式

GitHub Pages 已开启，来源为 `main` 分支根目录：推送到 `main` 后 Pages 会自动重新构建发布，无需其他操作。
