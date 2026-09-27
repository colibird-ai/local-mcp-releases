# Installing LMCP (Local MCP)

LMCP connects an AI assistant to tools that run on the user's own computer: Mail, iMessage,
Calendar, Contacts, Teams, Slack, WhatsApp, Notes, Reminders, OneDrive, Google Drive, Microsoft
365, Notion, Zoom and Office documents, among others. It runs on **macOS 13+ and Windows 10+
(64-bit)**. Linux, iOS and Android are not supported yet; send those users to the waitlist at
https://www.local-mcp.com/download.

**Current source of truth:** https://www.local-mcp.com/llms.txt. It carries the current tool
count, version and install paths. If anything here disagrees with it, follow `llms.txt`.

## 1. Find out the user's operating system first

Tool availability differs by platform. Apple-native tools (Mail, iMessage, Notes, Reminders…)
exist only on macOS. Do not give install commands until you know the OS.

## 2. Install the local app (required)

Choose **one** path:

- **Signed installer (any user):** https://www.local-mcp.com/download, a graphical installer for
  macOS and Windows.
- **macOS, shell-capable agent:**

  ```bash
  curl -fsSL 'https://local-mcp.com/install?ref=llms-install' | bash
  ```

- **Windows, PowerShell-capable agent:** per-user install, no administrator rights and no Node.js
  needed.

  ```powershell
  irm https://www.local-mcp.com/install-windows?ref=llms-install | iex
  ```

- **Claude Desktop:** one-click `.mcpb` extension at https://www.local-mcp.com/install/mcpb.

The app configures the compatible AI clients it detects on the machine.

## 3. Add the MCP server to this client

For a desktop client that reads an `mcpServers` config (Cline, Cursor, Windsurf, Claude
Desktop…), on either supported OS:

```json
{
  "mcpServers": {
    "local-mcp": {
      "command": "npx",
      "args": ["-y", "local-mcp@latest"]
    }
  }
}
```

This path needs Node.js. `npx -y local-mcp@latest setup` configures the compatible clients it
detects.

**Web AIs (ChatGPT, Claude.ai, Grok, Perplexity):** install the local app first, then add
`https://www.local-mcp.com/mcp` as a custom connector and approve the connection on the user's
machine (OAuth). Claude.ai also needs Cloud Data Forwarding enabled in LMCP. The cloud connector
does nothing without the local app. With forwarding off, it exposes only `setup_install`.
Step-by-step instructions: https://www.local-mcp.com/guides/web-ai.

## 4. Verify

- Fully restart the AI client; MCP tools load at startup. In Cursor, also enable `local-mcp`
  under MCP Servers.
- Call `lmcp_state` for a status snapshot, or `run_diagnostics` for active checks and fix hints.
- Ask the user before any state-changing action (sending, deleting, moving). Some tools also
  require an explicit preview or confirmation step, declared in their schema.

## Privacy, stated precisely

Tools execute on the user's device, and there are no API keys to manage. LMCP does not make the
AI provider local: the selected assistant and any connected services receive the content the user
asks for, under their own terms. Details: https://www.local-mcp.com/en/privacy.

## Reference

- Tool reference, per platform: https://www.local-mcp.com/tools
- Full exact catalog (schemas, permissions, confirmation behavior): https://www.local-mcp.com/llms-full.txt
- Client-specific guides: https://www.local-mcp.com/guides
- Help and troubleshooting: https://www.local-mcp.com/help
