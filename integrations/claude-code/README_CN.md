# Claude Code 集成

The Agency 是为 Claude Code 构建的。无需转换——agents 使用现有的 `.md` + YAML frontmatter 格式原生工作。

## 安装

```bash
# 复制所有 agents 到你的 Claude Code agents 目录
./scripts/install.sh --tool claude-code

# 或手动复制一个类别
cp engineering/*.md ~/.claude/agents/
```

## 激活 Agent

在任何 Claude Code 会话中，通过名称引用 agent：

```
Activate Frontend Developer and help me build a React component.
```

```
Use the Reality Checker agent to verify this feature is production-ready.
```

## Agent 目录

Agents 按部门组织。查看 [主 README](../../README.md) 了解完整的当前阵容。
