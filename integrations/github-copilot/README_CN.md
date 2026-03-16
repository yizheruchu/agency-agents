# GitHub Copilot 集成

The Agency 可以与 GitHub Copilot 原生配合使用。无需转换——agents 使用现有的 `.md` + YAML frontmatter 格式。

## 安装

```bash
# 复制所有 agents 到你的 GitHub Copilot agents 目录
./scripts/install.sh --tool copilot

# 或手动复制一个类别
cp engineering/*.md ~/.github/agents/
cp engineering/*.md ~/.copilot/agents/
```

## 激活 Agent

在任何 GitHub Copilot 会话中，通过名称引用 agent：

```
Activate Frontend Developer and help me build a React component.
```

```
Use the Reality Checker agent to verify this feature is production-ready.
```

## Agent 目录

Agents 按部门组织。查看 [主 README](../../README.md) 了解完整的当前阵容。
