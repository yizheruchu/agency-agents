# OpenCode 集成

OpenCode agents 是带有 YAML frontmatter 的 `.md` 文件，存储在 `.opencode/agents/`。转换器将命名颜色映射为十六进制代码，并添加 `mode: subagent`，以便 agents 通过 `@agent-name` 按需调用，而不是 cluttering 主 agent 选择器。

## 安装

```bash
# 从项目根目录运行
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool opencode
```

这会在项目目录中创建 `.opencode/agents/<slug>.md` 文件。

## 激活 Agent

在 OpenCode 中，使用 `@` 前缀调用 subagent：

```
@frontend-developer help build this component.
```

```
@reality-checker review this PR.
```

你也可以从 OpenCode UI 的 agent 选择器中选择 agents。

## Agent 格式

每个生成的 agent 文件包含：

```yaml
---
name: Frontend Developer
description: Expert frontend developer specializing in modern web technologies...
mode: subagent
color: "#00FFFF"
---
```

- **mode: subagent** — agent 在按需使用时可用，不显示在主 Tab 循环列表中
- **color** — 十六进制代码（源文件中的命名颜色会自动转换）

## 项目级与全局

`.opencode/agents/` 中的 agents 是**项目级的**。要使它们在所有项目中全局可用，请将它们复制到 OpenCode 配置目录：

```bash
mkdir -p ~/.config/opencode/agents
cp integrations/opencode/agents/*.md ~/.config/opencode/agents/
```

## 重新生成

```bash
./scripts/convert.sh --tool opencode
```
