# technical-analysis-notes

专门存放我与 Muse 协作完成的技术分析产物的公开仓库：交互式架构图、源码分析与深度拆解。所有网页产物通过 GitHub Pages 发布，可直接在线浏览。

在线浏览：https://hazirguo.github.io/technical-analysis-notes/

## 产物列表

| 日期 | 产物 | 说明 | 链接 |
|---|---|---|---|
| 2026-11-14 | HTTP CONNECT 指南 | HTTP CONNECT 的背景与演进（RFC 2817→9110→HTTP/2→MASQUE→CONNECT-IP）、为什么必须有 CONNECT 的三个原因、HTTPS 经代理的 12 个关键报文交互式时序图（每个报文含原始内容、逐字段表、抓包可见性与排障要点，精细到两次 TCP 三次握手与代理纯 SYN 拨号）、HTTP 代发与 HTTPS 隧道及 SOCKS5 对照、六大应用场景（含 HBONE、Kuasar Router→node proxy、MITM 位置 A/B）与 FAQ | [在线浏览](https://hazirguo.github.io/technical-analysis-notes/http-connect/) · [源码目录](./http-connect/) |
| 2026-11-09 | eBPF 可视化学习教程 | 面向 C/C++ 系统工程师的 11 章教程：从 cBPF 历史与内核模块之痛引入，详解 bpf() 系统调用、验证器、Maps、CO-RE / BTF、XDP、TC BPF、Socket 与 cgroup 钩子、NAT 与连接跟踪；以 Cilium 数据面为参照，最后落到沙箱网络转发面实战设计（veth 拓扑、五张 Map、M1–M5 落地里程碑）；含挂载点全景、验证器模拟器、Map 实验台、XDP 实验台、沙箱转发实验室五组交互演示与 8 题自测；以 RFC 9669 与内核 6.1+（tcx 需 6.6+）为准 | [在线浏览](https://hazirguo.github.io/technical-analysis-notes/ebpf-learning/) · [源码目录](./ebpf-learning/) |
| 2026-11-09 | CNI 可视化学习教程 | 面向 K8s 初学者的 13 章系统教程：从 Docker 网络之痛与 K8s 网络模型逐步引入，详解 CNI 规范 1.1.0、插件链与 IPAM、Overlay / BGP / 云 VPC 三种组网路线；Flannel、Calico、Cilium、Antrea、Kube-OVN、Multus 与云厂商 CNI 全景；含 Pod 接入、跨节点数据包旅程、NetworkPolicy、三问选型向导四组交互演示与自测；以 CNI 规范 1.1.0 为准 | [在线浏览](https://hazirguo.github.io/technical-analysis-notes/cni-learning/) · [源码目录](./cni-learning/) |
| 2026-11-09 | Istio 可视化学习教程 | 面向 K8s 初学者的 9 章系统教程：从微服务痛点与 K8s 能力边界逐步引入，详解 istiod / Envoy / xDS、Sidecar 与 Ambient（ztunnel + Waypoint）双数据面、流量管理、安全 mTLS 与授权、可观测性；含请求旅程、金丝雀、熔断、mTLS 四组交互演示与自测；以 Istio 1.31 为准 | [在线浏览](https://hazirguo.github.io/technical-analysis-notes/istio-learning/) · [源码目录](./istio-learning/) |
| 2026-11-04 | OpenKruise Agents 沙箱源码分析 | 基于源码 HEAD 20bbd53（710 个 Go 文件）逐项核实：Sandbox 本质是标准 Pod、17 个 CRD、预热池 Claim 与删 Pod 式 Pause、与 Envoy 同进程的 Go filter 入站网关与流量唤醒、出站由独立的 Agentio 栈实现（agentiod 策略编译与 DNS 主动解析、EPE 的 L7 执行、ztunnel 的 L4 执行，三仓记账）；含整体架构图与入站、出站双步进演示 | [在线浏览](https://hazirguo.github.io/technical-analysis-notes/openkruise-agents/) · [源码目录](./openkruise-agents/) |
| 2026-10-28 | 近期模型安全失控案例汇总 | 21 条案例分三类：A 真实逃逸/越界 7 起（Anthropic 四模型逃逸核实与三点修正、OpenAI 入侵 Hugging Face、DNS 隧道等）、B 部署事故 3 起、C 受控评测 11 条；附 13 种 containment 失效模式对照与 10 条沙箱工程师清单；可按类别筛选与关键词搜索 | [在线浏览](https://hazirguo.github.io/technical-analysis-notes/model-safety-incidents/) · [源码目录](./model-safety-incidents/) |
| 2026-10-26 | Muse 平台技术架构图 | 六层分层总览、一次请求的 7 步生命周期、Agent 协作拓扑、记忆系统、安全与信任边界、核心组件速览；可点击交互 | [在线浏览](https://hazirguo.github.io/technical-analysis-notes/muse-architecture/) · [源码目录](./muse-architecture/) |
| 2026-10-22 | vhost-xx 设备原理与场景 | 8 章：纯 virtio 三笔税、四种后端（纯 QEMU / vhost-net / vhost-user+DPDK / vDPA）数据面路径实验室、virtqueue 三环演示、7 步建立流程、9 个家族成员图鉴、拷贝次数对比、6 个应用场景、两问选型速判 | [在线浏览](https://hazirguo.github.io/technical-analysis-notes/vhost-xx/) · [源码目录](./vhost-xx/) |
| 2026-10-20 | Escaping SPACE 红队报告 · 中文汇报 | Perplexity 红队报告（2026-09-23）中文汇报：9 个前沿模型 108 次 VM 逃逸 0 成功、两种 egress 绕过手法（DNS 欺骗 / IP 共享 domain fronting）、修复与复测、10 家第三方沙箱横测与厂商响应、沙箱建设者检查清单 | [在线浏览](https://hazirguo.github.io/technical-analysis-notes/escaping-space/) · [源码目录](./escaping-space/) |

## 目录约定

- 每个产物一个顶层目录，目录名用 kebab-case，例如 `muse-architecture/`
- 产物入口统一为该目录下的 `index.html`（自包含单文件优先，避免资源依赖失效）
- 新增产物后，同步更新本表与根目录 `index.html` 索引页

## 发布方式

GitHub Pages 已开启，来源为 `main` 分支根目录：推送到 `main` 后 Pages 会自动重新构建发布，无需其他操作。
