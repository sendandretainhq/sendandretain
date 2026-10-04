# Send & Retain

Lifecycle email your agent runs — on your own Resend or SendGrid key.

**Using this from an AI agent? Read [AGENTS.md](./AGENTS.md).**

- **Docs** — https://sendandretain.com/docs
- **MCP endpoint** — `https://sendandretain.com/api/mcp` (OAuth 2.1, no token to mint)
- **Plugin** — [`sendandretain-plugin`](https://github.com/sendandretain/sendandretain-plugin) for Claude Code, Codex, Cursor, VS Code and other agent-plugin clients
- **SDKs** — [`sendandretain-node`](https://github.com/sendandretain/sendandretain-node) · [`sendandretain-py`](https://github.com/sendandretain/sendandretain-py)

## Quick start

```bash
claude mcp add --transport http sendandretain https://sendandretain.com/api/mcp
```

Then authorize in the browser when prompted. That is the whole setup — Send & Retain
uses OAuth, so there is no API token to copy around.

## What is in this repo

| File | |
| --- | --- |
| [`tools.json`](./tools.json) | All 83 MCP tools with JSON Schema |
| [`openapi.json`](./openapi.json) | REST API contract |
| [`AGENTS.md`](./AGENTS.md) | Orientation for coding agents |

The product is closed-source; this repo publishes its interface.

## Issues

Bug reports and API feedback are welcome here. For account or billing
questions use the in-app support channel instead.
