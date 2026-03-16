# 多代理工作流：带有持久内存的初创公司 MVP

> 与 [workflow-startup-mvp.md](workflow-startup-mvp.md) 中相同的初创公司 MVP 工作流，但使用 MCP 内存服务器在代理之间处理状态。不再需要复制粘贴交接。

## 手动交接的问题

在标准工作流中，每个代理到代理的转换看起来像这样：

```
Activate Backend Architect.

Here's our sprint plan: [paste Sprint Prioritizer output]
Here's our research brief: [paste UX Researcher output]

Design the API and database schema for RetroBoard.
...
```

你是胶水。你在代理之间复制粘贴输出，跟踪已完成的工作，并希望在此过程中不会丢失上下文。它适用于小型项目，但在以下情况下会崩溃：

- 会话超时时你会丢失输出
- 多个代理需要相同的上下文
- QA 失败，你需要回滚到先前的状态
- 项目跨越多天或多周的许多会话

## 解决方案

使用 MCP 内存服务器，代理将它们的交付物存储在内存中并自动检索所需内容。交接变成：

```
Activate Backend Architect.

Project: RetroBoard. Recall previous context for this project
and design the API and database schema.
```

代理搜索内存中的 RetroBoard 上下文，找到先前代理存储的冲刺计划和研究简报，然后从那里继续。

## 设置

安装任何支持 `remember`、`recall` 和 `rollback` 操作的 MCP 兼容内存服务器。设置请参阅 [integrations/mcp-memory/README.md](../integrations/mcp-memory/README.md)。

## 场景

与标准工作流相同：一个 SaaS 团队回顾工具（RetroBoard），4 周到 MVP，独立开发者。

## 代理团队

| 代理 | 在此工作流中的角色 |
|------|---------------------|
| Sprint Prioritizer | 将项目分解为每周冲刺 |
| UX Researcher | 通过快速用户访谈验证想法 |
| Backend Architect | 设计 API 和数据模型 |
| Frontend Developer | 构建 React 应用 |
| Rapid Prototyper | 快速运行第一个版本 |
| Growth Hacker | 在构建时规划发布策略 |
| Reality Checker | 在继续之前把关每个里程碑 |

每个代理的提示中都有一个 Memory Integration 部分（有关如何添加它，请参阅 [integrations/mcp-memory/README.md](../integrations/mcp-memory/README.md)）。

## 工作流

### 第 1 周：发现 + 架构

**Step 1 — 激活 Sprint Prioritizer**

```
Activate Sprint Prioritizer.

Project: RetroBoard — a real-time team retrospective tool for remote teams.
Timeline: 4 weeks to MVP launch.
Core features: user auth, create retro boards, add cards, vote, action items.
Constraints: solo developer, React + Node.js stack, deploy to Vercel + Railway.

Break this into 4 weekly sprints with clear deliverables and acceptance criteria.
Remember your sprint plan tagged for this project when done.
```

Sprint Prioritizer 生成冲刺计划并将其存储在内存中，标记为 `sprint-prioritizer`、`retroboard` 和 `sprint-plan`。

**Step 2 — 激活 UX Researcher（并行）**

```
Activate UX Researcher.

I'm building a team retrospective tool for remote teams (5-20 people).
Competitors: EasyRetro, Retrium, Parabol.

Run a quick competitive analysis and identify:
1. What features are table stakes
2. Where competitors fall short
3. One differentiator we could own

Output a 1-page research brief. Remember it tagged for this project when done.
```

UX Researcher 存储研究简报，标记为 `ux-researcher`、`retroboard` 和 `research-brief`。

**Step 3 — 移交给 Backend Architect**

```
Activate Backend Architect.

Project: RetroBoard. Recall the sprint plan and research brief from previous agents.
Stack: Node.js, Express, PostgreSQL, Socket.io for real-time.

Design:
1. Database schema (SQL)
2. REST API endpoints list
3. WebSocket events for real-time board updates
4. Auth strategy recommendation

Remember each deliverable tagged for this project and for the frontend-developer.
```

Backend Architect 自动从内存中检索冲刺计划和研究简报。无需复制粘贴。它存储其模式和 API 规范，标记为 `backend-architect`、`retroboard`、`api-spec` 和 `frontend-developer`。

### 第 2 周：构建核心功能

**Step 4 — 激活 Frontend Developer + Rapid Prototyper**

```
Activate Frontend Developer.

Project: RetroBoard. Recall the API spec and schema from the Backend Architect.

Build the RetroBoard React app:
- Stack: React, TypeScript, Tailwind, Socket.io-client
- Pages: Login, Dashboard, Board view
- Components: RetroCard, VoteButton, ActionItem, BoardColumn

Start with the Board view — it's the core experience.
Focus on real-time: when one user adds a card, everyone sees it.
Remember your progress tagged for this project.
```

Frontend Developer 从内存中提取 API 规范并据此构建。

**Step 5 — 中点检查**

```
Activate Reality Checker.

Project: RetroBoard. We're at week 2 of a 4-week MVP build.

Recall all deliverables from previous agents for this project.

Evaluate:
1. Can we realistically ship in 2 more weeks?
2. What should we cut to make the deadline?
3. Any technical debt that will bite us at launch?

Remember your verdict tagged for this project.
```

Reality Checker 完全可见迄今为止产生的所有内容——冲刺计划、研究简报、模式、API 规范和前端进度——无需你收集和粘贴所有内容。

### 第 3 周：完善 + 落地页面

**Step 6 — Frontend Developer 继续，Growth Hacker 启动**

```
Activate Growth Hacker.

Product: RetroBoard — team retrospective tool, launching in 1 week.
Target: Engineering managers and scrum masters at remote-first companies.
Budget: $0 (organic launch only).

Recall the project context and Reality Checker's verdict.

Create a launch plan:
1. Landing page copy (hero, features, CTA)
2. Launch channels (Product Hunt, Reddit, Hacker News, Twitter)
3. Day-by-day launch sequence
4. Metrics to track in week 1

Remember the launch plan tagged for this project.
```

### 第 4 周：发布

**Step 7 — 最终检查**

```
Activate Reality Checker.

Project: RetroBoard, ready to launch.

Recall all project context, previous verdicts, and the launch plan.

Evaluate production readiness:
- Live URL: [url]
- Test accounts created: yes
- Error monitoring: Sentry configured
- Database backups: daily automated

Run through the launch checklist and give a GO / NO-GO decision.
Require evidence for each criterion.
```

### 当 QA 失败时：回滚

在标准工作流中，当 Reality Checker 拒绝交付物时，你返回给负责的代理并试图解释出了什么问题。使用内存，恢复循环更紧密：

```
Activate Backend Architect.

Project: RetroBoard. The Reality Checker flagged issues with the API design.
Recall the Reality Checker's feedback and your previous API spec.
Roll back to your last known-good schema and address the specific issues raised.
Remember the updated deliverables when done.
```

Backend Architect 可以准确看到 Reality Checker 标记的内容，检索其先前的工作，回滚到检查点，并生成修复——所有这些都无需你手动跟踪版本。

## 前后对比

| 方面 | 标准工作流 | 使用内存 |
|------|------------|----------|
| **交接** | 在代理之间复制粘贴完整输出 | 代理自动检索所需内容 |
| **上下文丢失** | 会话超时丢失所有内容 | 内存在会话之间持久存在 |
| **多代理上下文** | 手动从 N 个代理编译上下文 | 代理搜索内存中的项目标签 |
| **QA 失败恢复** | 手动描述出了什么问题 | 代理检索反馈 + 回滚 |
| **多日项目** | 每次会话重新建立上下文 | 代理从上次离开的地方继续 |
| **所需设置** | 无 | 安装 MCP 内存服务器 |

## 关键模式

1. **用项目名称标记一切**：这是使检索工作的关键。每个内存都用 `retroboard`（或你的项目名称）标记。
2. **为接收代理标记交付物**：当 Backend Architect 完成 API 规范时，它将内存标记为 `frontend-developer`，以便 Frontend Developer 在检索时找到它。
3. **Reality Checker 获得完全可见性**：因为所有代理都将它们的工作存储在内存中，Reality Checker 可以检索项目的所有内容，无需你编译它。
4. **回滚替代手动撤销**：当某些内容失败时，回滚到最后一个检查点，而不是试图找出发生了什么变化。

## 提示

- 你不需要一次修改每个代理。首先通过向你最常使用的代理添加 Memory Integration 开始，然后从中扩展。
- 内存指令是提示，不是代码。LLM 根据需要解释它们并调用 MCP 工具。你可以调整措辞以匹配你的风格。
- 任何支持 `remember`、`recall`、`rollback` 和 `search` 工具的 MCP 兼容内存服务器都将与此工作流一起使用。
