# Gemini CLI 集成

将所有 61 个 Agency agents 打包为 Gemini CLI 扩展。扩展安装到 `~/.gemini/extensions/agency-agents/`。

## 安装

```bash
# 先生成 Gemini CLI 集成文件
./scripts/convert.sh --tool gemini-cli

# 然后安装扩展
./scripts/install.sh --tool gemini-cli
```

## 激活 Skill

在 Gemini CLI 中，通过名称引用 agent：

```
Use the frontend-developer skill to help me build this UI.
```

## 扩展结构

```
~/.gemini/extensions/agency-agents/
  gemini-extension.json
  skills/
    frontend-developer/SKILL.md
    backend-architect/SKILL.md
    reality-checker/SKILL.md
    ...
```

## 重新生成

```bash
./scripts/convert.sh --tool gemini-cli
```
