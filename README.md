# BlockReq Agent Skills

Agent Skills that teach AI coding assistants how to use [BlockReq](https://blockreq.com) RPC.

| Skill | What it covers |
| --- | --- |
| [`blockreq-rpc`](plugins/blockreq-rpc/skills/blockreq-rpc/SKILL.md) | EVM JSON-RPC through BlockReq: network hosts, the public trial versus an API key, WebSocket subscriptions, which networks serve archive, proof, debug, and trace methods, Request Counting and plan limits, and errors such as chain-ID mismatch, `429`, or missing historical state. |

The skill is generated from BlockReq's network and method catalogs by the Docs build and published at <https://blockreq.com/docs/agent-skills/blockreq-rpc/>. A daily workflow copies the published version into this repository, so do not edit the skill here.

## Install

**Claude Code**

```
/plugin marketplace add blockreq/skills
/plugin install blockreq-rpc@blockreq
```

Or copy `plugins/blockreq-rpc/skills/blockreq-rpc/` into `~/.claude/skills/` (all projects) or a project's `.claude/skills/`.

**Claude.ai:** download [blockreq-rpc.zip](https://blockreq.com/docs/agent-skills/blockreq-rpc.zip) and upload it as a custom skill. Custom skills need a Pro, Max, Team, or Enterprise plan with code execution enabled; see Anthropic's [Using Skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude) for where to upload.

**Other agents** that read Agent Skills: copy the `blockreq-rpc/` folder into the agent's skills directory.

More ways to use BlockReq with AI assistants (`llms.txt`, Markdown pages, OpenRPC, `networks.json`): <https://blockreq.com/docs/build/ai-assistants/>.

## 中文

教 AI 编程助手使用 [BlockReq](https://blockreq.com) RPC 的 Agent Skill。`blockreq-rpc` 由 BlockReq 文档构建从网络与方法目录生成，发布在 <https://blockreq.com/docs/agent-skills/blockreq-rpc/>；本仓库每天同步一次，请勿在此直接修改。

- Claude Code：`/plugin marketplace add blockreq/skills`，然后 `/plugin install blockreq-rpc@blockreq`；或把 `plugins/blockreq-rpc/skills/blockreq-rpc/` 复制到 `~/.claude/skills/`。
- Claude.ai：下载 [blockreq-rpc.zip](https://blockreq.com/docs/agent-skills/blockreq-rpc.zip)，作为自定义 Skill 上传（需 Pro、Max、Team 或 Enterprise 套餐并开启代码执行；上传入口见 Anthropic 的 [Using Skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude)）。
- 其他支持 Agent Skills 的助手：把 `blockreq-rpc/` 目录复制到其 skills 目录。
