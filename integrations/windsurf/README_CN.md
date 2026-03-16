# Windsurf 集成

所有 61 个 Agency agents 被合并到一个 `.windsurfrules` 文件中。规则是**项目级的**——请从项目根目录安装它们。

## 安装

```bash
# 从项目根目录运行
cd /your/project
/path/to/agency-agents/scripts/install.sh --tool windsurf
```

## 激活 Agent

在 Windsurf 中，在 prompt 中通过名称引用 agent：

```
Use the Frontend Developer agent to build this component.
```

## 重新生成

```bash
./scripts/convert.sh --tool windsurf
```
