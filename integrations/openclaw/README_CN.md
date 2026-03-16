# OpenClaw 集成

OpenClaw agents 被安装为包含 `SOUL.md`、`AGENTS.md` 和 `IDENTITY.md` 文件的工作区。安装器将每个工作区复制到 `~/.openclaw/agency-agents/`，并在 `openclaw` CLI 可用时注册它。

安装前，先生成 OpenClaw 工作区：

```bash
./scripts/convert.sh --tool openclaw
```

## 安装

```bash
./scripts/install.sh --tool openclaw
```

## 激活 Agent

安装后，agents 可通过 OpenClaw 会话中的 `agentId` 使用。

如果 OpenClaw gateway 已经在运行，请在安装后重启它：

```bash
openclaw gateway restart
```

## 重新生成

```bash
./scripts/convert.sh --tool openclaw
```
