# LMCP listing copy

One set of copy for every directory. Copy from here; do not rewrite per channel. Facts match the latest published version. Update this file first when the product changes, then update the listings (see `STATUS.md`).

## Rules for every listing

- Describe only what the published version does. No claims that exist only in a later version.
- No version numbers and no tool counts in copy that a third party hosts: nobody updates it after a release, so it goes stale (on 2026-10-09 the live listings said 82, 188+, 191+, 244, 255 and 290 tools). Use `@latest` in install lines. The release pipeline keeps the numbers that it writes itself (README, repository description).
- Nothing about pricing, plans, free tiers or charging. Do not write "free", "paid", "trial" or "premium".
- Do not add platform qualifiers such as "(Mac)" or "(Windows)" to an app name: every app named below works on Mac and Windows (WhatsApp and Outlook included; on the Mac, Outlook mail and calendar go through the Microsoft 365 tools). A limit of one platform belongs in its guide, not in listing copy.
- Say that the tools run on the user's computer, that the LMCP app is installed first, and that web AIs connect through an optional relay (Cloud Data Forwarding, off by default).
- Do not call it "100% local", "private" or "GDPR compliant". The AI provider still receives the content the user asks it to process.

## Identity

| Field | Value |
|---|---|
| Name | LMCP (package and server id: `local-mcp`) |
| Registry name | `com.local-mcp/local-mcp` |
| Tagline (30 characters or fewer) | `Your Mac and Windows apps` |
| Website | https://www.local-mcp.com |
| Repository (docs, plugins, releases) | https://github.com/colibird-ai/local-mcp-releases |
| Claude Code / Copilot CLI plugin repository | https://github.com/colibird-ai/local-mcp-claude-plugin |
| npm | https://www.npmjs.com/package/local-mcp |
| Install page | https://www.local-mcp.com/download |
| Agent install guide | https://github.com/colibird-ai/local-mcp-releases/blob/main/llms-install.md |
| Privacy | https://www.local-mcp.com/en/privacy |
| Support | support@local-mcp.com (security: see SECURITY.md) |
| Contact for directories | ctpo@colibird.co |
| Author / developer name | LMCP |
| Category | Productivity |
| Platforms | macOS 13+ and Windows 10+ (64-bit). Linux, iOS and Android are not supported. |
| Transport | stdio (`npx -y local-mcp@latest`); remote Streamable HTTP with OAuth at `https://www.local-mcp.com/mcp` for web AIs |
| License | Documentation, scripts and plugin manifests: MIT. The LMCP app binary is proprietary (see `LICENSE`). |

## Icon

- Repository file: `assets/logo.png` (512 x 512, PNG, transparent background) in https://github.com/colibird-ai/local-mcp-releases
- Hosted: https://www.local-mcp.com/icon-400.png (400 x 400)
- Screenshots: `assets/claude-tools.png`, `assets/tray-app.png`; demo: `assets/claude-web-demo.gif`

## Short description (use everywhere a single line is allowed)

> Local tools that let your AI use Mail, Calendar, Contacts, Teams, Slack, WhatsApp, OneDrive, Google Drive, Notion, Outlook and Office files on Mac and Windows. Runs on your computer.

Where a directory limits length, cut at a sentence boundary in this order and keep the first part:

1. Full text above (about 200 characters).
2. `Local tools for Mail, Calendar, Contacts, Teams, Slack, WhatsApp, OneDrive, Google Drive, Notion, Outlook and Office files. Mac and Windows.` (about 150 characters)
3. `Your Mac and Windows apps, as tools for your AI. Runs on your computer.` (about 70 characters)

## Long description (use everywhere a paragraph is allowed)

> LMCP is a local MCP server that lets your AI assistant work with the apps and files on your own computer. It provides tools for Mail, Calendar, Contacts, Microsoft Teams, Slack, WhatsApp, OneDrive, Google Drive, Notion, Outlook, Word, Excel, PowerPoint and PDF files, local files and more. Availability varies by platform.
>
> The tools run on your computer, on macOS 13+ and Windows 10+ (64-bit). Install the LMCP app first; your AI client then starts the server with `npx -y local-mcp@latest`, or through a plugin or extension for Claude Code, Codex, GitHub Copilot CLI, Gemini CLI and Cursor. Web assistants such as ChatGPT, Claude.ai, Grok and Perplexity connect through an optional relay at https://www.local-mcp.com/mcp using OAuth; it requires Cloud Data Forwarding, which is off by default.
>
> Permissions are granted per app, and you review actions before authorizing them. Your AI provider still receives the content you ask it to process. Documentation and manifests are MIT licensed; the LMCP app is proprietary.

## Keywords and topics

Repository topics (already set on `local-mcp-releases`): `mcp`, `mcp-server`, `claude`, `claude-code`, `codex`, `codex-plugin`, `cursor`, `cursor-plugin`, `gemini-cli-extension`, `github-copilot`, `chatgpt`, `macos`, `windows`, `email`, `imessage`, `whatsapp`, `productivity`, `privacy`, `local-first`, `ai-tools`.

Directory keywords (lowercase, hyphenated): `mcp`, `mail`, `calendar`, `contacts`, `teams`, `slack`, `whatsapp`, `onedrive`, `google-drive`, `notion`, `outlook`, `office`, `macos`, `windows`, `productivity`.

## Install lines

| Client | Line |
|---|---|
| Any MCP client | command `npx`, arguments `-y local-mcp@latest` |
| Claude Code | `claude plugin marketplace add colibird-ai/local-mcp-claude-plugin && claude plugin install local-mcp@local-mcp` |
| Codex CLI | `codex plugin marketplace add colibird-ai/local-mcp-releases && codex plugin add local-mcp@local-mcp` |
| GitHub Copilot CLI | `copilot plugin marketplace add colibird-ai/local-mcp-claude-plugin && copilot plugin install local-mcp@local-mcp` |
| Gemini CLI | `gemini extensions install https://github.com/colibird-ai/local-mcp-releases` |
| VS Code | `code --add-mcp '{"name":"local-mcp","command":"npx","args":["-y","local-mcp@latest"]}'` |
| Goose | `goose session --with-extension "npx -y local-mcp@latest"` |

The Claude Code, Codex, Copilot CLI and Gemini CLI lines work after the pull requests colibird-ai/local-mcp-claude-plugin#3 and colibird-ai/local-mcp-releases#49 are merged.

## Known copy to correct on the next publish

- Cline issue cline/mcp-marketplace#1909 still says "180 local Mac tools", "macOS only today" and "free": replace its title and body with the copy of section N of `SUBMISSIONS.md` (no tool count: rule above). The PR awesome-mcp-servers#15186 was corrected on 2026-10-09.
- The floor that the release pipeline writes is 201+ (`tool-count-floor.v1.json`). `local-mcp-claude-plugin` still says 192+ in its README and repository description, and the npm description still ends in "free": both are written by `lmcp-npm` (#61).
