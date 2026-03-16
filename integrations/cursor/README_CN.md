# Cursor 集成

将所有 61 个 Agency agents 转换为 Cursor `.mdc` 规则文件。规则是**项目级的**——请从项目根目录安装它们。

## 安装

```bash
# 从项目根目录运行
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool cursor
```

这会在项目中创建 `.cursor/rules/<agent-slug>.mdc` 文件。

## 激活规则

在 Cursor 中，在 prompt 中引用 agent：

```
@frontend-developer Review this React component for performance issues.
```

或者通过编辑 frontmatter 将规则启用为始终应用：

```yaml
---
description: Expert frontend developer...
globs: "**/*.tsx,**/*.ts"
alwaysApply: true
---
```

## 重新生成

```bash
./scripts/convert.sh --tool cursor
```
