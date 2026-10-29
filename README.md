### 余诺 · YN
[continueyn.site](https://www.continueyn.site) · [GitHub](https://github.com/ContinueYN) · [Repositories](https://github.com/ContinueYN?tab=repositories)

---
## 概览
面向 LLM 应用的全栈交付，覆盖接入层、编排层、数据层与可观测链路。前端以 Vue 承担复杂交互，AI 侧覆盖检索增强、工具调用与多 Agent 编排。
关注三类指标：检索质量（召回率、重排效果、上下文预算）、推理时延（TTFT、输出吞吐）、失败路径的可恢复性（超时、降级、幂等重试）。
## 能力域
| 域 | 交付物 | 核心问题 |
| :-- | :-- | :-- |
| **LLM 应用** | 企业级智能体：RAG 知识库、工具调用、MCP、多 Agent 协作 | 召回精度、上下文预算、工具幂等与超时降级 |
| **服务端** | 单体到微服务拆分与治理，缓存分层、分布式锁、分库分表 | 缓存击穿与雪崩、热点行、慢查询、一致性边界 |
| **前端** | WebGPU / Three.js 实时渲染、滚动叙事、3D 角色交互 | 帧预算、GC 压力、上下文丢失恢复、降级策略 |
| **交付与可观测** | 容器化、反向代理、全链路追踪与告警 | p99 时延、错误预算、SLO、灰度与回滚 |
## 项目
- **[Portfolio Website](https://github.com/ContinueYN/Website)**：个人站点，WebGPU 渲染与滚动叙事（[在线](https://www.continueyn.site)）
  - 80 块碎面经 `BatchedMesh` 合批为单次绘制，噪声缩放在拼合相位收敛至 1；TSL 节点材质做菲涅尔边缘光，后处理以 Sobel 深度描边叠 Bayer 抖动抑制暗部色带。
- **[GomokuMind](https://github.com/ContinueYN/GomokuMind)**：五子棋策略评估与辅助决策
  - 启发式评估、Minimax、Alpha-Beta 剪枝、MCTS、AlphaZero 式策略并行基线，搜索树与评估函数可视化。
- **[SynapseMind](https://github.com/ContinueYN/SynapseMind)**：单题诊断式学习引导
  - 以 2–6 轮追问收敛至最早失效的认知动作，基于神经可塑性与 CHC 七维模型做归因，产出带证据链的卡点报告。
- **[ChatRegistry-AI](https://github.com/ContinueYN/ChatRegistry-AI)**：全栈对话系统
  - FastAPI 双服务拆分，SSE 流式输出、多轮上下文管理、思维链与 Markdown 增量渲染，GLM-4 函数调用。
- **[dsh-vscode](https://github.com/ContinueYN/dsh-vscode)**：编码智能体的编辑器侧接入
  - 会话生命周期、工具调用与文件差异的可视化，降低终端与编辑器之间的上下文切换成本。
- **[Poem](https://github.com/ContinueYN/Poem)**：三维诗词展示
  - Three.js 渲染管线与装帧状态机，卷轴、册页、竹简多形态切换，粒子与光影分层叠加。
## 技术栈
`Java` `Python` `Go` `TypeScript` `Vue 3`
`Spring Cloud` `MySQL` `Redis` `Caffeine` `PGvector` `Docker` `Nginx`
`Spring AI` `LangChain4j` `MCP` `Prometheus` `Grafana` `ARMS`
## 工程实践
- **规格驱动**：需求固化为可验证约束（Spec-Kit / OpenSpec），评审对象从实现细节前移到边界条件与失败路径。
- **评测闭环**：固定 golden set 做回归，提示词与检索参数变更先离线评测再进主干。
- **可复现 harness**：模型、工具、上下文与评测同环境运行，换模型即换基线，结论可比较。
- **可观测**：trace / span 覆盖检索、工具调用与生成三段，故障定位到单次请求级别。
## 方向
- 检索链路：混合召回与重排策略，向量库与业务库的一致性边界
- 智能体工程：MCP Server 与 Agent Skills 的复用与权限收敛
- 成本与时延：缓存命中率、上下文裁剪、批量推理与降级路径
---
