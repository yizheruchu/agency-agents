# Antigravity 集成

安装所有 61 个 Agency agents 作为 Antigravity skills。每个 agent 以 `agency-` 为前缀，以避免与现有 skills 冲突。

## 安装

```bash
./scripts/install.sh --tool antigravity
```

这会将文件从 `integrations/antigravity/` 复制到 `~/.gemini/antigravity/skills/`。

## 激活 Skill

在 Antigravity 中，通过其 slug 激活 agent：

```
Use the agency-frontend-developer skill to review this component.
```

可用的 slugs 遵循模式 `agency-<agent-name>`，例如：
- `agency-frontend-developer`
- `agency-backend-architect`
- `agency-reality-checker`
- `agency-growth-hacker`

## 重新生成

修改 agents 后，重新生成 skill 文件：

```bash
./scripts/convert.sh --tool antigravity
```

## 文件格式

每个 skill 是一个带有 Antigravity 兼容 frontmatter 的 `SKILL.md` 文件：

```yaml
---
name: agency-frontend-developer
description: Expert frontend developer specializing in...
risk: low
source: community
date_added: '2026-03-08'
---
```
