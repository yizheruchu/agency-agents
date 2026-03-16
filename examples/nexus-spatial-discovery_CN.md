# Nexus Spatial: 完整 Agency 发现练习

> **练习类型：** 多 agent 产品发现
> **日期：** 2026 年 3 月 5 日
> **部署 agents：** 8 个（并行）
> **持续时间：** 约 10 分钟实际时间
> **目的：** 展示从机会识别到全面规划的完整 agency 编排

---

## 目录

1. [机会](#1-机会)
2. [市场验证](#2-市场验证)
3. [技术架构](#3-技术架构)
4. [品牌战略](#4-品牌战略)
5. [上市与增长](#5-上市与增长)
6. [客户支持蓝图](#6-客户支持蓝图)
7. [UX 研究与设计方向](#7-ux-研究与设计方向)
8. [项目执行计划](#8-项目执行计划)
9. [空间接口架构](#9-空间接口架构)
10. [跨 Agent 综合](#10-跨-agent-综合)

---

## 1. 机会

### 如何发现的

通过对多个来源的网络研究，确定了三个汇聚的趋势：

- **AI 基础设施/编排** 是增长最快的软件类别（AI 编排市场在 2026 年价值约 135 亿美元，年复合增长率 22%+）
- **空间计算**（Vision Pro、WebXR）正在成熟，但缺乏杀手级企业应用
- 每个现有的 AI 工作流工具（LangSmith、n8n、Flowise、CrewAI）都是**扁平的 2D 仪表板**

### 概念：Nexus Spatial

空间计算中的 AI Agent 指挥中心——一个 VisionOS + WebXR 应用，提供沉浸式 3D 指挥中心，用于编排、监控和与 AI agents 交互。用户将 agent 管道可视化为 3D 节点图，在空间面板中监控实时输出，在 3D 空间中通过拖放构建工作流，并在共享空间环境中协作。

### 为什么这个 Agency 具有独特优势

该 agency 拥有深厚的空间计算专业知识（XR 开发人员、VisionOS 工程师、Metal 专家、接口架构师），以及完整的工程、设计、营销和运营团队——这对于需要空间计算掌握和企业软件严谨性的产品来说是罕见的组合。

### 来源

- [Profitable SaaS Ideas 2026 (273K+ Reviews)](https://bigideasdb.com/profitable-saas-micro-saas-ideas-2026)
- [2026 SaaS and AI Revolution: 20 Top Trends](https://fungies.io/the-2026-saas-and-ai-revolution-20-top-trends/)
- [Top 21 Underserved Markets 2026](https://mktclarity.com/blogs/news/list-underserved-niches)
- [Fastest Growing Products 2026 - G2](https://www.g2.com/best-software-companies/fastest-growing)
- [PwC 2026 AI Business Predictions](https://www.pwc.com/us/en/tech-effect/ai-analytics/ai-predictions.html)

---

## 2. 市场验证

**Agent:** Product Trend Researcher

### 结论：CONDITIONAL GO——2D 优先，空间第二

### 市场规模

| 细分市场 | 2026 年价值 | 增长 |
|---------|-----------|------|
| AI 编排工具 | 135 亿美元 | 22.3% 年复合增长率 |
| 自主 AI Agents | 85 亿美元 | 45.8% 年复合增长率，到 2030 年达 503 亿美元 |
| 扩展现实 | 106.4 亿美元 | 40.95% 年复合增长率 |
| 空间计算（广义） | 1700-2200 亿美元 | 因定义而异 |

### 竞争格局

**AI Agent 编排（全部 2D）：**

| 工具 | 优势 | UX 差距 |
|------|----------|--------|
| LangChain/LangSmith | 基于图的编排，$39/用户/月 | 扁平仪表板；复杂图在规模下不可读 |
| CrewAI | 100K+ 开发人员，快速执行 | CLI 优先，最小可视化工具 |
| Microsoft Agent Framework | 企业集成 | 嵌入 Azure 门户，无独立 UI |
| n8n | 可视化工作流构建器，$20-50/月 | 2D 画布难以处理 agent 关系 |
| Flowise | 拖放 AI 流 | 限于线性流，无多 agent 监控 |

**"Mission Control"产品（新兴，全部 2D）：**
- cmd-deck：AI 编码 agents 的 Kanban 板
- Supervity Agent Command Center：企业可观测性
- OpenClaw Command Center：Agent 舰队管理
- Mission Control AI：合成工人管理
- Mission Control HQ：基于小队的协调

**差距：** 产品要么是空间但不以 AI 为中心，要么是以 AI 为中心但扁平 2D。没有产品位于交叉点。

### Vision Pro 现实检查

- 安装基数：全球约 100 万台（销量从发布时下降 95%）
- Apple 已将重点转向轻量化 AR 眼镜
- 仅存在约 3,000 个 VisionOS 特定应用
- **含义：** 不要以 VisionOS 为主。以 web 为主，添加 WebXR，原生 VisionOS 最后。

### WebXR 作为分发解锁

- Safari 在 2025 年末采用 WebXR Device API
- 2026 年 WebXR 采用率增长 40%
- WebGPU 在浏览器中提供接近原生的渲染
- Android XR 支持 WebXR 和 OpenXR 标准

### 目标角色和定价

| 层级 | 价格 | 目标 |
|------|------|------|
| Explorer | 免费 | 开发人员、独立构建者（3 个 agents，WebXR 查看器） |
| Pro | $99/用户/月 | 小团队（25 个 agents，协作） |
| Team | $249/用户/月 | 中端市场 AI 团队（无限 agents，分析） |
| Enterprise | 定制（$2K-10K/月） | 大型企业（SSO、RBAC、本地部署、SLA） |

### 推荐的分阶段策略

1. **第 1-6 个月：** 构建具有 Three.js 2.5D 功能的高级 2D web 仪表板。目标：50 个付费团队，$60K MRR。
2. **第 6-12 个月：** 添加可选 WebXR 空间模式（基于浏览器）。目标：200 个团队，$300K MRR。
3. **第 12-18 个月：** 仅当空间需求得到验证时才开发原生 VisionOS 应用。目标：500 个团队，$1M+ MRR。

### 关键风险

| 风险 | 严重程度 |
|------|----------|
| Vision Pro 安装基数 critically 小 | 高 |
| "寻找问题的空间解决方案"——3D 真的比 2D 好 10 倍吗？ | 高 |
| 拥挤的"mission control"定位（已有 5+ 产品） | 中等 |
| 企业空间计算采用仍早期 | 中等 |
| 跨 AI 框架的集成复杂性 | 中等 |

### 来源

- [MarketsandMarkets - AI Orchestration Market](https://www.marketsandmarkets.com/Market-Reports/ai-orchestration-market-148121911.html)
- [Deloitte - AI Agent Orchestration Predictions 2026](https://www.deloitte.com/us/en/insights/industry/technology/technology-media-and-telecom-predictions/2026/ai-agent-orchestration.html)
- [Mordor Intelligence - Extended Reality Market](https://www.mordorintelligence.com/industry-reports/extended-reality-xr-market)
- [Fintool - Vision Pro Production Halted](https://fintool.com/news/apple-vision-pro-production-halt)
- [MadXR - WebXR Browser-Based Experiences 2026](https://www.madxr.io/webxr-browser-immersive-experiences-2026.html)

---

## 3. 技术架构

**Agent:** Backend Architect

### 系统概述

一个 8 服务架构，具有清晰的所有权边界，设计用于水平扩展和提供商无关的 AI 集成。

```
+------------------------------------------------------------------+
|                     客户端层                                       |
|  VisionOS 原生 (Swift/RealityKit)  |  WebXR (React Three Fiber)  |
+------------------------------------------------------------------+
                              |
+-----------------------------v------------------------------------+
|                      API 网关 (Kong / AWS API GW)                 |
|  速率限制 | JWT 验证 | WebSocket 升级 | TLS                      |
+------------------------------------------------------------------+
                              |
+------------------------------------------------------------------+
|                      服务层                                       |
|  认证 | 工作区 | 工作流 | 编排 (Rust) |                          |
|  协作 (Yjs CRDT) | 流式传输 (WS) | 插件 | 计费                   |
+------------------------------------------------------------------+
                              |
+------------------------------------------------------------------+
|                      数据层                                       |
|  PostgreSQL 16 | Redis 7 集群 | S3 | ClickHouse | NATS          |
+------------------------------------------------------------------+
                              |
+------------------------------------------------------------------+
|                    AI 提供商层                                    |
|  OpenAI | Anthropic | Google | 本地模型 | 自定义插件             |
+------------------------------------------------------------------+
```

### 技术栈

| 组件 | 技术 | 理由 |
|-----------|------------|-----------|
| 编排引擎 | **Rust** | 亚毫秒调度，零 GC 停顿，内存安全用于 agent 沙箱 |
| API 服务 | TypeScript / NestJS | CRUD 密集型服务的开发人员速度 |
| VisionOS 客户端 | Swift 6, SwiftUI, RealityKit | 具有 Liquid Glass 的一流空间计算 |
| WebXR 客户端 | TypeScript, React Three Fiber | 具有 React 组件模型的生产级 WebXR |
| 消息代理 | NATS JetStream | 轻量级，精确一次交付，比 Kafka 简单 |
| 协作 | Yjs (CRDT) + WebRTC | 无冲突的并发 3D 图编辑 |
| 主数据库 | PostgreSQL 16 | JSONB 用于灵活配置，行级安全用于租户隔离 |

### 核心数据模型

14 个表涵盖：
- **身份和访问：** users, workspaces, team_memberships, api_keys
- **工作流：** workflows, workflow_versions, nodes, edges
- **执行：** executions, execution_steps, step_output_chunks
- **协作：** collaboration_sessions, session_participants
- **凭据：** provider_credentials (AES-256-GCM 加密)
- **计费：** subscriptions, usage_records
- **审计：** audit_log (仅追加)

### 节点类型注册表

```
内置节点类型：
  ai_agent          -- 使用 prompt 调用 AI 提供商
  prompt_template   -- 使用变量渲染模板
  conditional       -- 基于表达式路由
  transform         -- 沙箱代码片段 (JS/Python)
  input / output    -- 工作流入口/出口点
  human_review      -- 暂停等待人工批准
  loop              -- 重复子图
  parallel_split    -- 分支扇出
  parallel_join     -- 等待分支
  webhook_trigger   -- 外部 HTTP 触发器
  delay             -- 定时暂停
```

### WebSocket 通道

通过 WSS 实时流式传输：
- 每个通道的序列号用于排序
- 间隙检测与重放请求
- 当落后 >1000 个事件时的快照恢复
- 客户端节流用于低功耗设备

### 安全架构

| 层 | 机制 |
|-------|-----------|
| 用户认证 | OAuth 2.0 (GitHub, Google, Apple) + 邮箱/密码 + 可选 TOTP MFA |
| API Keys | SHA-256 哈希，范围限定，可选过期 |
| 服务间通信 | mTLS 通过 service mesh |
| WebSocket 认证 | 一次性 ticket，30 秒过期 |
| 凭据存储 | 信封加密 (AES-256-GCM + AWS KMS) |
| 代码沙箱 | gVisor/Firecracker microVMs（无网络，256MB RAM，30s CPU） |
| 租户隔离 | PostgreSQL 行级安全 + S3 IAM 策略 + NATS 主题范围限定 |

### 扩展目标

| 指标 | 第 1 年 | 第 2 年 |
|--------|--------|--------|
| 并发 agent 执行 | 5,000 | 50,000 |
| WebSocket 连接 | 10,000 | 100,000 |
| P95 API 延迟 | < 150ms | < 100ms |
| P95 WS 事件延迟 | < 80ms | < 50ms |

### MVP 阶段

1. **第 1-6 周：** 2D web 编辑器，顺序执行，OpenAI + Anthropic 适配器
2. **第 7-12 周：** WebXR 3D 模式，并行执行，手部追踪，RBAC
3. **第 13-20 周：** 多用户协作，VisionOS 原生，计费
4. **第 21-30 周：** 企业 SSO，插件 SDK，SOC 2，扩展加固

---

## 4. 品牌战略

**Agent:** Brand Guardian

### 定位

**类别创建胜过类别竞争。** Nexus Spatial 定义了一个新类别——**Spatial AI Operations (SpatialAIOps)**——而不是在拥挤的 AI 可观测性仪表板空间中争夺位置。

**定位声明：** 对于管理复杂 AI agent 工作流的技术团队，Nexus Spatial 是沉浸式 3D 指挥中心，提供 agent 编排的空间意识，与扁平 2D 仪表板不同，因为空间计算将监控从阅读仪表板转变为驻留在基础设施中。

### 名称验证

"Nexus Spatial"被**验证为强大：**
- "Nexus"连接到 NEXUS 编排框架（Network of EXperts, Unified in Strategy）
- "Nexus"独立意味着"中央连接点"——非常适合指挥中心
- "Spatial"是 Apple 和行业已标准化的行业标准描述符
- 语音平衡：三个音节，然后两个
- **需要行动：** 在 Nice 第 9、42 和 38 类进行商标许可

### 品牌个性：指挥官

| 特质 | 表达 | 避免 |
|-------|------------|--------|
| **权威性** | 清晰、直接、技术精确 | 炒作、最高级、模糊未来主义 |
| **镇定** | 干净设计、有节奏的白色空间 | 为紧迫而紧迫、混乱 |
| **开拓性** | 安静的自豪、对新范式的低调引用 | "革命性"、"改变游戏规则" |
| **精确** | 精确规格、真实指标、诚实要求 | 模糊声明、营销行话 |
| **亲和** | 自然交互语言、空间隐喻 | 居高临下、守门 |

### 标语（排名）

1. **"Mission Control for the Agent Era"**——推荐主标语
2. "See Your Agents in Space"
3. "Orchestrate in Three Dimensions"
4. "Where AI Operations Become Spatial"
5. "Command Center. Reimagined in Space."
6. "The Dimension Your Dashboards Are Missing"
7. "AI Agents Deserve More Than Flat Screens"

### 颜色系统

| 颜色 | Hex | 用途 |
|-------|-----|-------|
| Deep Space Indigo | `#1B1F3B` | 基础深色画布、背景 |
| Nexus Blue | `#4A7BF7` | 签名品牌、主要操作 |
| Signal Cyan | `#00D4FF` | 空间高亮、数据连接 |
| Command Green | `#00E676` | 健康系统、成功 |
| Alert Amber | `#FFB300` | 警告、需要注意 |
| Critical Red | `#FF3D71` | 错误、失败 |

使用比例：Deep Space Indigo 60%，Nexus Blue 25%，Signal Cyan 10%，语义 5%。

### 排版

- **Primary:** Inter（UI、正文、标签）
- **Monospace:** JetBrains Mono（代码、日志、agent 输出）
- **Display:** Space Grotesk（仅营销标题）

### Logo 概念

三个探索方向：

1. **The Spatial Nexus Mark**——汇聚线在发光中央节点交汇，具有微妙的透视深度
2. **The Dimensional Window**——风格化视口，具有透视线，创造看向 3D 空间的效果
3. **The Orbital Array**——围绕中心点的轨道环，暗示协调 agents 在运动中

### 品牌价值

- **Spatial Truthfulness**——诚实表示系统状态，无 cosmetic 平滑
- **Operational Gravity**——为生产构建，不是演示
- **Dimensional Generosity**——WebXR 确保空间价值对每个人可访问
- **Composure Under Complexity**——系统越复杂，界面越冷静

### Design Tokens

```css
:root {
  --nxs-deep-space:       #1B1F3B;
  --nxs-blue:             #4A7BF7;
  --nxs-cyan:             #00D4FF;
  --nxs-green:            #00E676;
  --nxs-amber:            #FFB300;
  --nxs-red:              #FF3D71;
  --nxs-void:             #0A0E1A;
  --nxs-slate-900:        #141829;
  --nxs-slate-700:        #2A2F45;
  --nxs-slate-500:        #4A5068;
  --nxs-slate-300:        #8B92A8;
  --nxs-slate-100:        #C8CCE0;
  --nxs-cloud:            #E8EBF5;
  --nxs-white:            #F8F9FC;
  --nxs-font-primary:     'Inter', sans-serif;
  --nxs-font-mono:        'JetBrains Mono', monospace;
  --nxs-font-display:     'Space Grotesk', sans-serif;
}
```

---

## 5. 上市与增长

**Agent:** Growth Hacker

### 北极星指标

**Weekly Active Pipelines (WAP)**——过去 7 天内至少有一次空间交互的唯一 agent 管道。捕捉创建和参与，与价值相关，不易被操纵。

### 定价

| 层级 | 年付 | 月付 | 目标 |
|------|--------|---------|--------|
| Explorer | 免费 | 免费 | 3 个管道，WebXR 预览，社区 |
| Pro | $29/用户/月 | $39/用户/月 | 无限管道，VisionOS，30 天历史 |
| Team | $59/用户/月 | $79/用户/月 | 协作，RBAC，SSO，90 天历史 |
| Enterprise | 定制（约$150+） | 定制 | 专用基础设施，SLA，本地部署选项 |

策略：14 天反向试用（Pro 功能，然后降级到免费）。目标 5-8% 免费到付费转化。

### 3 阶段 GTM

**第 1 阶段：创始人主导销售（第 1-3 个月）**
- 目标：使用 LangChain/CrewAI 并拥有 Vision Pro 的初创公司独立 AI 工程师
- 策略：DM 200 名高知名度 AI 工程师，每周 build-in-public 帖子，30 秒演示剪辑
- 渠道：X/Twitter、LinkedIn、AI 专注 Discord 服务器、Reddit

**第 2 阶段：开发者社区（第 4-6 个月）**
- Product Hunt 发布（针对此阶段定时，不是第 1 阶段）
- Hacker News Show HN、Dev.to 文章、会议演讲
- 与流行 AI 框架的集成公告

**第 3 阶段：企业（第 7-12 个月）**
- Apple 企业推荐渠道，LinkedIn ABM 活动
- 企业案例研究，分析师简报（Gartner、Forrester）
- 第一位企业 AE 招聘，SOC 2 合规

### 增长循环

1. **"Wow Factor"演示循环**——空间演示天生可分享。一键"Share Spatial Preview"生成 WebXR 链接或视频。目标 K = 0.3-0.5。
2. **模板市场**——高级用户发布管道模板，可通过搜索发现，驱动新注册。
3. **协作席位扩展**——一位工程师采用，与队友分享，团队扩展到付费计划（Slack/Figma 剧本）。
4. **集成驱动发现**——在 LangChain、n8n、OpenAI/Anthropic 合作伙伴目录中列出。

### 开源策略

**开源（Apache 2.0）：**
- `nexus-spatial-sdk`——TypeScript/Python SDK 用于连接 agent 框架
- `nexus-webxr-components`——React Three Fiber 组件库用于 3D 管道
- `nexus-agent-schemas`——标准化 schema 用于在 3D 中表示 agent 管道

**保持专有：** VisionOS 原生应用、协作引擎、企业功能、托管基础设施。

### 收入目标

| 指标 | 第 6 个月 | 第 12 个月 |
|--------|---------|----------|
| MRR | $8K-15K | $50K-80K |
| 免费账户 | 5,000 | 15,000 |
| 付费席位 | 300 | 1,200 |
| Discord 成员 | 2,000 | 5,000 |
| GitHub stars (SDK) | 500 | 2,000 |

### 首个$50K 预算

| 类别 | 金额 | % |
|----------|--------|---|
| 内容制作 | $12,000 | 24% |
| 开发者关系 | $10,000 | 20% |
| 付费获取测试 | $8,000 | 16% |
| 社区和工具 | $5,000 | 10% |
| Product Hunt 和发布 | $3,000 | 6% |
| 开源维护 | $3,000 | 6% |
| PR 和 outreach | $4,000 | 8% |
| 合作伙伴关系 | $2,000 | 4% |
| 储备 | $3,000 | 6% |

### 关键合作伙伴关系

- **Tier 1（关键）：** Anthropic、OpenAI——一流 API 集成、合作伙伴计划列表
- **Tier 2（采用）：** LangChain、CrewAI、n8n——框架集成、社区交叉传播
- **Tier 3（平台）：** Apple——Vision Pro 开发者套件、App Store 推荐、WWDC
- **Tier 4（生态系统）：** GitHub、Hugging Face、Docker——开发者平台集成

### 来源

- [AI Orchestration Market Size - MarketsandMarkets](https://www.marketsandmarkets.com/Market-Reports/ai-orchestration-market-148121911.html)
- [Spatial Computing Market - Precedence Research](https://www.precedenceresearch.com/spatial-computing-market)
- [How to Price AI Products - Aakash Gupta](https://www.news.aakashg.com/p/how-to-price-ai-products)
- [Product Hunt Launch Guide 2026](https://calmops.com/indie-hackers/product-hunt-launch-guide/)

---

## 6. 客户支持蓝图

**Agent:** Support Responder

### 支持层级结构

| 属性 | Explorer (免费) | Builder (Pro) | Command (企业) |
|-----------|-----------------|---------------|---------------------|
| 首次响应 SLA | 尽力而为 (48h) | 4 小时（工作时间） | 30 分钟 (P1), 2h (P2) |
| 解决 SLA | 5 个工作日 | 24h (P1/P2), 72h (P3) | 4h (P1), 12h (P2) |
| 渠道 | 社区、KB、AI 助手 | + 在线聊天、邮件、视频 (2/月) | + 专用 Slack、指定 CSE、24/7 |
| 范围 | 一般问题、文档 | 技术故障排除、集成 | 完整集成、自定义设计、合规 |

### 优先级定义

- **P1 Critical：** 编排宕机、数据丢失风险、安全漏洞
- **P2 High：** 主要功能降级，存在变通方案
- **P3 Medium：** 非阻塞问题、小故障
- **P4 Low：** 功能请求、cosmetic 问题

### The Nexus Guide：AI 驱动的产品内支持

突出的设计决策：支持 agent 作为可见节点生活在**用户的空间工作区内部**。它完全了解用户的布局、活跃 agents 和最近错误。

**能力：**
- 关于功能的自然语言问答
- 实时 agent 诊断（"为什么 Agent X 慢？"）
- 配置建议（"你的拓扑作为 mesh 性能会更好"）
- 引导式空间故障排除演练
- 自动附加上下文的工单创建

**自愈：**

| 场景 | 检测 | 自动解决 |
|----------|-----------|-----------------|
| Agent 无限循环 | CPU/token 峰值 | 终止并以最后良好配置重启 |
| 渲染帧下降 | FPS 低于阈值 | 降低视觉保真度，建议关闭面板 |
| 凭据过期 | API 401 响应 | 提示重新认证，优雅暂停 agents |
| 通信超时 | 延迟峰值 | 通过备用路径重新路由消息 |

### Onboarding 流程

基于用户画像的自适应 onboarding：

| AI 经验 | 空间经验 | 路径 |
|---------------|-------------------|------|
| 低 | 低 | 完整引导游览 (20 分钟) |
| 高 | 低 | 空间聚焦 (12 分钟) |
| 低 | 高 | Agent 聚焦 (12 分钟) |
| 高 | 高 | 快速设置 (5 分钟) |

关键第一步：60 秒空间校准（手部追踪、注视、舒适度检查），然后才能进行任何产品交互。

**激活里程碑**（当用户拥有以下内容时视为"已 onboarding"）：
- 创建至少一个自定义 agent
- 连接两个或更多 agents 到拓扑中
- 固定至少一个监控仪表板
- 返回第三次会话

### 团队构建

| 阶段 | 人数 | 角色 |
|-------|-----------|-------|
| 0-6 个月 | 4 | CX 负责人、2 名支持工程师、技术文档撰写人 |
| 6-12 个月 | 8 | + 2 名支持工程师、CSE、社区经理、运营分析师 |
| 12-24 个月 | 16 | + 4 名工程师 (24/7)、空间专家、集成专家、KB 管理员、工程经理 |

### 社区：Discord 优先

```
NEXUS SPATIAL DISCORD
  信息：#announcements, #changelog, #status
  支持：#help-getting-started, #help-agents, #help-spatial
  讨论：#general, #show-your-workspace, #feature-requests
  平台：#visionos, #webxr, #api-and-sdk
  活动：office-hours (每周语音), community-demos (每月)
  PRO 成员：#pro-lounge, #beta-testing
  企业：每个客户的私人渠道
```

**Champions Program ("Nexus Navigators")：** 5-10 名初始高级用户，具有 Navigator 徽章，与产品团队的直接 Slack，免费 Pro 层级，早期功能访问，以及年度峰会。

---

## 7. UX 研究与设计方向

**Agent:** UX Researcher

### 用户角色

**Maya Chen——AI 平台工程师（32 岁，旧金山）**
- 管理 15-30 个活跃 agent 工作流，使用 n8n + LangSmith
- 花费 40% 时间通过日志检查调试 agent 故障
- 对空间计算持怀疑态度："这真的更快，还是只是更酷？"
- 主要需求：将平均诊断时间从 45 分钟减少到 10 分钟以下

**David Okoro——技术产品经理（38 岁，伦敦）**
- 审查和批准 agent 工作流设计，向 C-suite 展示
- 无法有意义地参与工作流审查，因为工具需要代码级理解
- 主要需求：在不阅读代码的情况下理解和传达 agent 架构

**Dr. Amara Osei——研究科学家（45 岁，苏黎世）**
- 设计具有 A/B 比较的多 agent 研究工作流
- 有 12 个相同管道的变体，没有好的比较方法
- 主要需求：在 3D 空间中并排比较变体管道

**Jordan Rivera——创意技术专家（27 岁，奥斯汀）**
- 每日 Vision Pro 用户，构建 AI 驱动的艺术装置
- 想要感觉像乐器而不是仪表板的工具
- 主要需求：快速构建 agent 工作流，具有即时空间反馈

### 关键发现：调试是杀手级用例

工作流结构上的运行时跟踪空间叠加解决了一个真实的、量化的痛点，没有 2D 工具能很好地处理。这个工作流应该获得最多的设计和工程投资。

### 关键设计洞察

空间为**结构化**任务（放置、连接、重新排列节点）增加价值，但为**参数**任务（文本输入、配置）创造摩擦。界面必须无缝融合空间和 2D 模式——锚定在空间位置的 2D 面板。

### 7 个设计原则

1. **Spatial Earns Its Place**——如果 2D 更清晰，使用 2D。每次审查都应该问："这样扁平会更好吗？"
2. **Glanceable Before Inspectable**——关键信息在 2 秒内通过颜色、大小、运动、位置可感知
3. **Hands-Free Is the Baseline**——注视 + 语音覆盖所有读取/导航操作；手增加精度但不是必需的
4. **Respect Cognitive Gravity**——扩展 2D 心理模型（从左到右流），不要替换它们；z 轴添加分层
5. **Progressive Spatial Complexity**——新用户从近乎 2D 开始；随着信心增长，空间功能逐渐展现
6. **Physical Metaphors, Digital Capabilities**——节点被"拿起"（物理），但也被复制和版本化（数字）
7. **Silence Is a Feature**——健康系统感觉平静；颜色和运动信号偏离正常

### 导航范式：4 级语义缩放

| 级别 | 你看到什么 |
|-------|-------------|
| Fleet View | 所有工作流作为抽象形状，按状态颜色编码 |
| Workflow View | 节点图，带有标签和连接 |
| Node View | 扩展配置、最近 I/O、状态指标 |
| Trace View | 完整执行跟踪，带有数据检查 |

### 竞争 UX 摘要

| 能力 | n8n | Flowise | LangSmith | Langflow | Nexus Spatial 目标 |
|-----------|-----|---------|-----------|----------|---------------------|
| 可视化工作流构建 | A | B+ | N/A | A | A+ (空间) |
| 调试/跟踪 | C+ | C | A | B | A+ (空间叠加) |
| 监控 | B | C | A | B | A (空间舰队) |
| 协作 | D | D | C | D | A (空间共存) |
| 大型工作流可扩展性 | C | C | B | C | A (3D 空间) |

### 无障碍要求

- 每个交互可通过至少两种模态实现
- 没有信息仅通过颜色传达
- 高对比度模式、减少运动模式、深度扁平化模式
- 屏幕阅读器兼容空间元素描述
- 每 20-30 分钟会话长度警告
- 所有核心任务可坐姿、单手、在 30 度移动锥内完成

### 研究计划（16 周）

| 阶段 | 周 | 研究 |
|-------|-------|---------|
| 基础 | 1-4 | 心理模型访谈（15-20 名参与者）、竞争任务分析 |
| 概念验证 | 5-8 | Wizard-of-Oz 空间原型测试、IA 3D 卡片分类 |
| 可用性测试 | 9-14 | 首次使用体验（20 用户）、4 周长跑日记研究、配对协作测试 |
| 无障碍审计 | 12-16 | 专家启发式评估、与残障用户测试 |

---

## 8. 项目执行计划

**Agent:** Project Shepherd

### 时间线：35 周（2026 年 3 月 9 日 - 11 月 6 日）

| 阶段 | 周 | 持续时间 | 目标 |
|-------|-------|----------|------|
| 发现与研究 | W1-3 | 3 周 | 验证可行性、定义范围 |
| 基础 | W4-9 | 6 周 | 核心基础设施、两个平台 shell、设计系统 |
| MVP 构建 | W10-19 | 10 周 | 单用户 agent 指挥中心，具有编排 |
| Beta | W20-27 | 8 周 | 协作、打磨、加固、50-100 beta 用户 |
| 发布 | W28-31 | 4 周 | App Store + web 发布、营销推动 |
| 扩展 | W32-35+ | 持续 | 插件市场、高级功能、增长 |

### 关键里程碑：第 12 周（5 月 29 日）

**首次端到端工作流执行。** 用户在 3D 中创建并运行 3 节点 agent 工作流。这是产品证明其核心价值主张的时刻。如果这个延迟，所有下游都会转移。

### 前 6 个 Sprints（65 个 Tickets）

**Sprint 1（3 月 9-20 日）：** VisionOS SDK 审计、WebXR 兼容性矩阵、编排引擎可行性、利益相关者访谈、两个平台的 throwaway 原型。

**Sprint 2（3 月 23 日 - 4 月 3 日）：** 架构决策记录、MVP 范围锁定（MoSCoW）、PRD v1.0、空间 UI 模式研究、交互模型定义、设计系统启动。

**Sprint 3（4 月 6-17 日）：** Monorepo 设置、认证服务 (OAuth2)、数据库 schema、API 网关、VisionOS Xcode 项目初始化、WebXR 项目初始化、CI/CD 管道。

**Sprint 4（4 月 20 日 - 5 月 1 日）：** WebSocket 服务器 + 客户端 SDK、空间窗口管理、3D 组件库、手部追踪输入层、teams CRUD、集成测试。

**Sprint 5（5 月 4-15 日）：** 编排引擎核心 (Rust)、agent 状态机、节点图渲染器（两个平台）、插件接口 v0、OpenAI 提供商插件。

**Sprint 6（5 月 18-29 日）：** 工作流持久化 + 版本控制、DAG 执行、实时执行可视化、Anthropic 提供商插件、眼动追踪集成、空间音频。

### 团队分配

5 个小队在各个阶段运作：

| 小队 | 核心成员 | 活跃阶段 |
|-------|-------------|---------------|
| 核心架构 | Backend Architect、XR Interface Architect、高级开发、VisionOS 工程师 | 发现到 MVP |
| 空间体验 | XR Immersive 开发、XR Cockpit 专家、Metal 工程师、UX 架构师、UI 设计师 | 基础到 Beta |
| 编排 | AI 工程师、Backend Architect、高级开发、API 测试员 | MVP 到 Beta |
| 平台交付 | 前端开发、移动应用构建器、VisionOS 工程师、DevOps | MVP 到发布 |
| 发布 | Growth Hacker、Content Creator、App Store 优化师、视觉故事讲述者、Brand Guardian | Beta 到扩展 |

### 前 5 大风险

| 风险 | 概率 | 影响 | 缓解 |
|------|------------|--------|------------|
| Apple 拒绝 VisionOS 应用 | 中等 | 关键 | 第 4 周联系 Apple 开发者关系，第 20 周预审 |
| WebXR 浏览器碎片化 | 高 | 高 | 第 1 周浏览器支持矩阵、自动化跨浏览器测试 |
| 多用户同步冲突 | 中等 | 高 | 从一开始就使用基于 CRDT 的同步 (Yjs)，在基础阶段原型化 |
| 编排无法扩展 | 中等 | 关键 | 从第一天起就水平扩展，第 22 周进行 10 倍负载测试 |
| RealityKit 对 100+ 节点的性能 | 中等 | 高 | 早期分析、实现 LOD 剔除、实例化渲染 |

### 预算：$121,500 -- $155,500（非人员）

| 类别 | 估计成本 |
|----------|---------------|
| 云基础设施（35 周） | $35,000 - $45,000 |
| 硬件（3 台 Vision Pro、2 台 Quest 3、Mac Studio） | $17,500 |
| 许可证和服务 | $15,000 - $20,000 |
| 外部服务（法律、安全、PR） | $30,000 - $45,000 |
| AI API 成本（开发/测试） | $8,000 |
| 应急（15%） | $16,000 - $20,000 |

---

## 9. 空间接口架构

**Agent:** XR Interface Architect

### The Command Theater

工作区组织为围绕用户的弯曲剧院：

```
                        OVERVIEW CANOPY
                     (管道拓扑)
                    ~~~~~~~~~~~~~~~~~~~~~~~~
                   /                        \
                  /     FOCUS ARC (120 度)   \
                 /    主要节点图工作   \
                /________________________________\
               |                                  |
    左侧       |        用户位置             |       右侧
    工具栏    |        (原点 0,0,0)            |       工具栏
               |__________________________________|
                \                                /
                 \      SHELF (视线下方) /
                  \   agent 状态、快速工具/
                   \_________________________ /
```

- **Focus Arc**（120 度，1.2-2.0m）：主要节点图工作区
- **Overview Canopy**（上方，2.5-4.0m）：微型管道拓扑 + 健康热图
- **Utility Rails**（左/右翼）：Agent 库、监控、日志
- **Shelf**（视线下方，0.8-1.0m）：运行/停止、撤销/重做、快速工具

### 三层深度系统

| 层 | 深度 | 内容 | 不透明度 |
|-------|-------|---------|---------|
| 前景 | 0.8 - 1.2m | 活动面板、检查器、模态框 | 100% |
| 中景 | 1.2 - 2.5m | 节点图、连接、工作区 | 100% |
| 背景 | 2.5 - 5.0m | 概览图、环境状态 | 40-70% |

### 3D 节点图

**数据流向用户。** 节点沿 z 轴按执行顺序排列：

```
用户 (这里)
  z=0.0m   [输出节点]     -- 结果
  z=0.3m   [转换节点]  -- 处理器
  z=0.6m   [Agent 节点]      -- LLM 调用
  z=0.9m   [检索节点]  -- RAG、APIs
  z=1.2m   [输入节点]      -- 触发器
```

并行分支水平传播（x 轴）。条件分支垂直传播（y 轴）。

**节点表示（3 LODs）：**
- **LOD-0**（静止，>1.5m）：12x8cm 磨砂玻璃矩形，带有类型图标、名称、状态光晕
- **LOD-1**（悬停，400ms 注视）：扩展到 14x10cm，显示端口、上次运行信息
- **LOD-2**（选中）：滑到前景，扩展到 30x40cm 详细面板，带有实时配置编辑

**连接作为发光管：**
- 静止时直径 4mm，携带数据时 8mm
- 按数据类型颜色编码（白色=文本、青色=结构化、品红=图像、琥珀色=音频、绿色=工具调用）
- 动画粒子显示流动方向和速度
- 当>3 个在同一层之间平行运行时自动捆绑

### 7 个 Agent 状态

| 状态 | 边缘光晕 | 内部 | 声音 | 粒子 |
|-------|-----------|----------|-------|-----------|
| Idle | 稳定绿色，低 | 静态磨砂玻璃 | 无 | 无 |
| Queued | 脉冲琥珀色，1Hz | 微弱旋转 | 无 | 输入处缓慢漂移 |
| Running | 稳定蓝色，中等 | 动画闪烁 | 柔和空间嗡嗡声 | 连接上快速流动 |
| Streaming | 蓝色 + 输出流 | 闪烁 + 文本片段 | 嗡嗡声 | 文本片段向前流动 |
| Completed | 闪烁白色，然后绿色 | 静态 | 完成钟声 | 无 |
| Error | 脉冲红色，2Hz | 红色色调 | 警报音（一次） | 无 |
| Paused | 稳定琥珀色 | 冻结帧 + 暂停图标 | 无 | 冻结在原位 |

### 交互模型

| 操作 | VisionOS | WebXR 控制器 | 语音 |
|--------|----------|-------------------|-------|
| 选择节点 | 注视 + 捏合 | 指向射线 + 触发 | "Select [name]" |
| 移动节点 | 捏合 + 拖动 | 抓握 + 移动 | -- |
| 连接端口 | 捏合端口 + 拖动 | 触发端口 + 拖动 | "Connect [A] to [B]" |
| 平移工作区 | 双手拖动 | 摇杆 | "Pan left/right" |
| 缩放 | 双手展开/捏合 | 摇杆推/拉 | "Zoom in/out" |
| 检查节点 | 捏合 + 向自己拉 | 双触发 | "Inspect [name]" |
| 运行管道 | 点击 Shelf 按钮 | 触发按钮 | "Run pipeline" |
| 撤销 | 两指双击 | B 按钮 | "Undo" |

### 协作存在

每个协作者由以下表示：
- **头部代理：** 半透明球体，带有个人资料图像，随头部方向旋转
- **手部代理：** 幽灵手模型，显示捏合/抓握状态
- **注视锥：** 微妙的 10 度锥，显示他们看的方向
- **名称标签：** 广告牌渲染，显示当前操作（"editing Node X"）

**冲突解决：** 第一位编辑者获得写锁；第二位看到"locked by [name]"，可选择请求访问或复制节点。

### 自适应布局

| 环境 | 节点比例 | 最大 LOD-2 节点 | 图 Z 扩展 |
|-------------|-----------|-----------------|----------------|
| VisionOS 窗口 | 4x3cm | 5 | 0.05m/层 |
| VisionOS 沉浸式 | 12x8cm | 15 | 0.3m/层 |
| WebXR 桌面 | 120x80px | 8（覆盖） | 透视投影 |
| WebXR 沉浸式 | 12x8cm | 12 | 0.3m/层 |

### 过渡编排

所有过渡服务于寻路。主要过渡最多 600ms，次要 200ms，选择 0ms。

| 过渡 | 持续时间 | 关键运动 |
|-----------|----------|------------|
| 概览到聚焦 | 600ms | 相机漂移到目标，其他区域淡出到 30% |
| 聚焦到详细 | 500ms | 节点向前滑动、扩展、连接高亮 |
| 详细到概览 | 600ms | 面板折叠、节点后退、完整拓扑可见 |
| 区域切换 | 500ms | 当前横向滑出、新滑入 |
| 窗口到沉浸式 | 1000ms | 边框溶解、节点扩展到完整空间位置 |

### 舒适度措施

- 无用户操作时不启动相机移动
- 稳定地平线（水平面永不倾斜）
- 主要交互在 0.8-2.5m 内，视线 +/-15 度
- 45 分钟后休息提示（环境光照变化，非模态）
- 快速移动时外围暗角
- 所有常用控件在手臂两侧可访问（仅手腕/手指）

---

## 10. 跨 Agent 综合

### 所有 8 个 Agents 的一致点

1. **2D 优先，空间第二。** 每个 agent 独立得出这个结论。首先构建一个优秀的 web 仪表板，然后逐步添加空间功能。

2. **调试是杀手级用例。** Product Researcher、UX Researcher 和 XR Interface Architect 都汇聚于此：工作流结构上的运行时跟踪空间叠加是 3D 真正击败 2D 的地方。

3. **WebXR 胜过 VisionOS 用于初始覆盖。** Vision Pro 的约 100 万安装基数无法维持业务。浏览器中的 WebXR 是分发解锁。

4. **"war room"协作场景。** 多个 agents 强调协当事件响应作为最强的空间价值主张——团队进入共享 3D 空间一起调试失败的管道。

5. **渐进式披露至关重要。** UX Research、Spatial UI 和 Support 都强调空间复杂性必须逐渐展现，绝不能倾倒在首次用户身上。

6. **语音作为高级用户加速器。** UX Researcher 和 XR Interface Architect 都将语音命令识别为"空间计算的命令行"——对于无障碍和专家效率至关重要。

### 需要解决的关键张力

| 张力 | 立场 A | 立场 B | 需要的解决方案 |
|---------|-----------|-----------|-------------------|
| **定价** | Growth Hacker: $29-59/用户/月 | Trend Researcher: $99-249/用户/月 | beta 中 A/B 测试 |
| **VisionOS 优先级** | 架构：第 3 阶段（第 13 周+） | 空间 UI：完整规范就绪 | 先构建 WebXR，验证后再做 VisionOS |
| **编排语言** | 架构：Rust | 项目计划：未指定 | Rust 对于性能关键的 DAG 执行是正确的 |
| **MVP 范围** | 架构：第 1 阶段仅 2D | 品牌：以空间为主 | 2D 优先，但确保每次演示都有空间 |
| **社区平台** | 支持：Discord 优先 | 营销：Discord + 开源 | 两者——Discord 用于社区，GitHub 用于开发者参与 |

### 这个练习展示的内容

本发现文档由 8 个专业 agents 并行生成，每个 agent 为共同目标带来深厚的领域专业知识。Agents 独立得出一致的结论，同时揭示领域特定的洞察，这些洞察对于任何单一通才来说都难以产生：

- **Product Trend Researcher** 发现了令人清醒的 Vision Pro 销售数据，重新构建了整个战略
- **Backend Architect** 设计了没有营销聚焦团队会考虑的 Rust 编排引擎
- **Brand Guardian** 创建了一个类别（"SpatialAIOps"），而不是在现有类别中竞争
- **UX Researcher** 发现空间计算为参数任务创造摩擦——一个反直觉的发现
- **XR Interface Architect** 设计了"数据流向你"的拓扑，映射到自然空间认知
- **Project Shepherd** 识别了可能破坏整个时间线的三个关键瓶颈角色
- **Growth Hacker** 设计了特定于空间计算固有可分享性的病毒循环
- **Support Responder** 将产品自己的 AI 能力转化为支持差异化

结果是一个全面的、跨职能的产品计划，可以作为实际开发的基础——由 AI agents 协作机构在单次会议中生成。
