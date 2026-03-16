# 示例

本目录包含示例输出，展示如何编排 agency 的 agents 来完成真实世界的任务。

## 为什么存在这个目录

agency-agents 仓库定义了数十个专业 agents，分布在工程、设计、营销、产品、支持、空间计算和项目管理等部门。但仅凭 agents 定义并不能展示当你**一次性部署所有 agents**执行单一任务时会发生什么。

这些示例回答了这个问题：*"当整个 agency 协作时，实际上是什么样子？"*

## 内容

### [nexus-spatial-discovery.md](./nexus-spatial-discovery_CN.md)

**内容：** 一个完整的产品发现练习，8 个 agents 并行工作以评估软件机会并产生统一计划。

**场景：** 网络研究发现了 AI agent 编排和空间计算交叉点的机会。然后同时部署整个 agency 来生成：

- 市场验证和竞争分析
- 技术架构（8 服务系统设计，包含完整 SQL schema）
- 品牌战略和视觉识别
- 上市和增长计划
- 客户支持运营蓝图
- UX 研究计划，包含角色和旅程地图
- 35 周项目执行计划，包含 65 个 sprint tickets
- 空间接口架构规范

**使用的 agents：**
| Agent | 角色 |
|-------|------|
| Product Trend Researcher | 市场验证，竞争格局 |
| Backend Architect | 系统架构，数据模型，API 设计 |
| Brand Guardian | 定位，视觉识别，命名 |
| Growth Hacker | GTM 策略，定价，发布计划 |
| Support Responder | 支持层级，onboarding，社区 |
| UX Researcher | 角色，旅程地图，设计原则 |
| Project Shepherd | 阶段计划，sprints，风险登记 |
| XR Interface Architect | 空间 UI 规范 |

**关键要点：** 所有 8 个 agents 并行运行，生成连贯的、交叉引用的计划，无需协调开销。输出展示了 agency 从"发现机会"到"这是完整蓝图"的单会话能力。

## 添加新示例

如果你运行了有趣的多 agent 练习，考虑添加到这里。好的示例展示：

- 多个 agents 协作完成共同目标
- agency 能力的广度
- agent 定义的真实世界适用性
