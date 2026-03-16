# 🔌 集成

本目录包含 The Agency 的集成方案和已转换格式，支持多种 agentic 编程工具。

## 支持的工具

- **[Claude Code](#claude-code)** — `.md` agents，直接使用仓库文件
- **[GitHub Copilot](#github-copilot)** — `.md` agents，直接使用仓库文件
- **[Antigravity](#antigravity)** — 每个 agent 对应 `antigravity/` 中的 `SKILL.md`
- **[Gemini CLI](#gemini-cli)** — 扩展 + `gemini-cli/` 中的 `SKILL.md` 文件
- **[OpenCode](#opencode)** — `.md` agent 文件位于 `opencode/`
- **[OpenClaw](#openclaw)** — `SOUL.md` + `AGENTS.md` + `IDENTITY.md` 工作区
- **[Cursor](#cursor)** — `cursor/` 中的 `.mdc` 规则文件
- **[Aider](#aider)** — `aider/` 中的 `CONVENTIONS.md`
- **[Windsurf](#windsurf)** — `windsurf/` 中的 `.windsurfrules`

## 快速安装

```bash
# 自动安装到所有检测到的工具
./scripts/install.sh

# 安装特定的全局工具
./scripts/install.sh --tool antigravity
./scripts/install.sh --tool copilot
./scripts/install.sh --tool openclaw
./scripts/install.sh --tool claude-code

# Gemini CLI 在全新克隆后需要生成集成文件
./scripts/convert.sh --tool gemini-cli
./scripts/install.sh --tool gemini-cli
```

对于项目级工具（如 OpenCode、Cursor、Aider 和 Windsurf），需要从目标项目根目录运行安装脚本，如下面各工具特定部分所示。

## 重新生成集成文件

如果添加或修改了 agents，请重新生成所有集成文件：

```bash
./scripts/convert.sh
```

---

## Claude Code

The Agency 最初是为 Claude Code 构建的。Agents 无需转换即可原生工作。

```bash
cp -r <category>/*.md ~/.claude/agents/
# 或一次性安装所有内容：
./scripts/install.sh --tool claude-code
```

详见 [claude-code/README.md](claude-code/README.md)。

---

## GitHub Copilot

The Agency 也可以与 GitHub Copilot 原生配合使用。Agents 可以直接复制到
`~/.github/agents/` 和 `~/.copilot/agents/`，无需转换。

```bash
./scripts/install.sh --tool copilot
```

详见 [github-copilot/README.md](github-copilot/README.md)。

---

## Antigravity

Skills 安装到 `~/.gemini/antigravity/skills/`。每个 agent 成为一个独立的 skill，
使用前缀 `agency-` 以避免命名冲突。

```bash
./scripts/install.sh --tool antigravity
```

详见 [antigravity/README.md](antigravity/README.md)。

---

## Gemini CLI

Agents 被打包为带有独立 skill 文件的 Gemini CLI 扩展。
扩展安装到 `~/.gemini/extensions/agency-agents/`。
由于 Gemini manifest 和 skill 文件夹是生成的产物，因此在全新克隆后需要先运行
`./scripts/convert.sh --tool gemini-cli`，然后再安装。

```bash
./scripts/convert.sh --tool gemini-cli
./scripts/install.sh --tool gemini-cli
```

详见 [gemini-cli/README.md](gemini-cli/README.md)。

---

## OpenCode

每个 agent 成为一个项目级的 `.md` 文件，位于 `.opencode/agents/`。

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool opencode
```

详见 [opencode/README.md](opencode/README.md)。

---

## OpenClaw

每个 agent 成为一个 OpenClaw 工作区，包含 `SOUL.md`、`AGENTS.md` 和 `IDENTITY.md`。

安装前，先生成 OpenClaw 工作区：

```bash
./scripts/convert.sh --tool openclaw
```

然后安装：

```bash
./scripts/install.sh --tool openclaw
```

详见 [openclaw/README.md](openclaw/README.md)。

---

## Cursor

每个 agent 成为一个 `.mdc` 规则文件。规则是项目级的——请从项目根目录运行安装脚本。

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool cursor
```

详见 [cursor/README.md](cursor/README.md)。

---

## Aider

所有 agents 被合并到一个 `CONVENTIONS.md` 文件中，Aider 会在项目根目录自动读取它。

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool aider
```

详见 [aider/README.md](aider/README.md)。

---

## Windsurf

所有 agents 被合并到一个 `.windsurfrules` 文件中，放在项目根目录。

```bash
cd /your/project && /path/to/agency-agents/scripts/install.sh --tool windsurf
```

详见 [windsurf/README.md](windsurf/README.md)。
