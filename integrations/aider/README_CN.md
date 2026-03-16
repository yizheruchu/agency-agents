# Aider 集成

所有 61 个 Agency agents 被合并到一个 `CONVENTIONS.md` 文件中。Aider 在项目根目录存在此文件时会自动读取它。

## 安装

```bash
# 从项目根目录运行
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool aider
```

## 激活 Agent

在 Aider 会话中，通过名称引用 agent：

```
Use the Frontend Developer agent to refactor this component.
```

```
Apply the Reality Checker agent to verify this is production-ready.
```

## 手动使用

你也可以直接传递 conventions 文件：

```bash
aider --read CONVENTIONS.md
```

## 重新生成

```bash
./scripts/convert.sh --tool aider
```
