# Send & Retain

Email automation your agent runs — sending included, unlimited contacts.

**Using this from an AI agent? Read [AGENTS.md](./AGENTS.md).**

- **Docs** — https://sendandretain.com/docs
- **MCP endpoint** — `https://sendandretain.com/api/mcp` (OAuth 2.1, no token to mint)
- **Plugin** — [`sendandretain-plugin`](https://github.com/sendretain/sendandretain-plugin) for Claude Code, Codex, Cursor, VS Code and other agent-plugin clients
- **SDKs** — [`sendandretain-node`](https://github.com/sendretain/sendandretain-node) · [`sendandretain-py`](https://github.com/sendretain/sendandretain-py)

## Quick start

```bash
claude mcp add --transport http sendandretain https://sendandretain.com/api/mcp
```

Then authorize in the browser when prompted. That is the whole setup — Send & Retain
uses OAuth, so there is no API token to copy around.

From your own application, use an SDK with a key from **Settings → API keys**:

```ts
import { SendAndRetain } from "@sendandretain/sdk"; // npm install @sendandretain/sdk

const { data, error } = await new SendAndRetain().emails.send({ to: "jane@acme.com", template: "welcome" });
```

```python
from sendandretain import SendAndRetain  # pip install sendandretain

email = SendAndRetain().emails.send(to="jane@acme.com", template="welcome")
```

## What is in this repo

| File | |
| --- | --- |
| [`tools.json`](./tools.json) | Every MCP tool with its JSON Schema (`toolCount` is the live number) |
| [`openapi.json`](./openapi.json) | REST API contract (OpenAPI 3.1, semver in `info.version`), including the payload of every webhook event |
| [`AGENTS.md`](./AGENTS.md) | Orientation for coding agents |

The product is closed-source; this repo publishes its interface.

## Issues

Bug reports and API feedback are welcome here. For account or billing
questions use the in-app support channel instead.
