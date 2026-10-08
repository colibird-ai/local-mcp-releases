# Listing status

Single tracking table for every AI-tool directory. Last checked: 2026-10-08 (REST and web checks only). Copy lives in `DESCRIPTIONS.md`; ready-to-paste payloads in `SUBMISSIONS.md` (letters in the last column refer to its sections). Update this table whenever a status changes.

Legend: Listed = visible in the directory. Open = submitted, waiting for the directory. Prepared = payload ready, waiting for the step named. Needs Dario = a form, login, email or merge only he can do. Not applicable = the channel has no listing we can use.

| Channel | Method | Status | Link | Next step |
|---|---|---|---|---|
| MCP Registry (official) | `mcp-publisher` from `lmcp-npm` CI | Listed. 3.0.419 is active and latest (older versions deprecated). | https://registry.modelcontextprotocol.io/v0.1/servers?search=com.local-mcp | On the next publish replace the description that ends in "Free." (see `DESCRIPTIONS.md`). This registry also covers Zed and Goose (below). |
| Glama | Crawl plus `glama.json` | Listed | https://glama.ai/mcp/servers/colibird-ai/local-mcp-releases | None. |
| Smithery | CLI publish from CI | Listed | https://smithery.ai/server/@lanchuske/local-mcp | None. |
| TensorBlock MCP index | Pull request | Listed (PR merged 2026-09-27) | https://tensorblock.co/mcp/servers/github-lanchuske-local-mcp-releases-bf301799 | None. |
| mcpm.sh registry | Pull request | Listed (PR merged 2026-10-06) | https://github.com/pathintegral-institute/mcpm.sh/pull/410 | None. |
| Cline MCP Marketplace | Issue form in cline/mcp-marketplace | Open since 2026-08-27, no maintainer reply. Nudge posted 2026-10-08 with Windows support, install line and org URL. | https://github.com/cline/mcp-marketplace/issues/1909 | Check in one week; do not open another issue (two earlier ones were closed as duplicates). |
| awesome-mcp-servers (punkpeye) | Pull request | Open. Mergeable, 2 bot comments: `missing-glama` (badge is already in the entry) and `duplicate` (false positive: the PR edits the existing entry). Last activity 2026-09-27. | https://github.com/punkpeye/awesome-mcp-servers/pull/15186 | Wait. Do not open another PR: ten earlier ones were closed. Update the "188+ tools" text to 192+ only if a maintainer asks for changes. |
| awesome-mac (jaywcjlove) | Pull request | Open since 2026-07-28 | https://github.com/jaywcjlove/awesome-mac/pull/2442 | Wait. |
| mcp.so | Issue in chatmcp/mcpso | Open since 2026-05-08 (stale) | https://github.com/chatmcp/mcpso/issues/1341 | Submit the form on mcp.so with the new copy (needs Dario's login); the issue text is outdated. |
| GitHub Copilot: github/copilot-plugins | Pull request (marketplace.json plus README) | Open, opened 2026-10-08 from the `lanchuske` fork | https://github.com/github/copilot-plugins/pull/104 | Wait. Third-party pull requests there (#87 to #103) have not been merged; GitHub curates this list. |
| GitHub Copilot: github/awesome-copilot | Issue form `external-plugin.yml`, immutable ref plus SHA | Prepared. Waits for colibird-ai/local-mcp-claude-plugin#3 and a release tag. | https://github.com/github/awesome-copilot/issues/new?template=external-plugin.yml | Needs Dario (merge #3). Then tag and file the issue: `SUBMISSIONS.md` section C. |
| Claude plugin directory (Anthropic) | Web form | Prepared. Needs #3 merged. | https://clau.de/plugin-directory-submission | Needs Dario: submit the form. `SUBMISSIONS.md` section A. |
| Claude Code marketplace (own repo) | `.claude-plugin/marketplace.json` in the plugin repo | Pull request open | https://github.com/colibird-ai/local-mcp-claude-plugin/pull/3 | Needs Dario: squash merge. |
| Cursor Marketplace | Web form, manual review, open source required | Not listed (checked: cursor.com/marketplace/local-mcp shows "Marketplace Plugin Not Found"). Manifest already on `main`. | https://cursor.com/marketplace/publish | Needs Dario: submit the repository link while logged in. `SUBMISSIONS.md` section B. |
| Codex: community list (hashgraph-online/awesome-codex-plugins) | README line plus scanner score of 80/130 or higher | Prepared. Needs releases#49 merged and a clean scanner run. | https://github.com/hashgraph-online/awesome-codex-plugins | After merge: run the scanner, then open the pull request (`SUBMISSIONS.md` section D). A lockfile is missing. |
| Codex: official OpenAI plugin directory | Portal at platform.openai.com/plugins | Prepared. Heavy requirements. | https://developers.openai.com/plugins/deploy/submission | Needs Dario: decide, then verify the developer identity and upload (section D). |
| Gemini CLI extensions gallery | Daily crawl of GitHub topic `gemini-cli-extension` | Not listed. Topic is set; `gemini-extension.json` arrives with releases#49. | https://geminicli.com/extensions | Needs Dario: merge #49. Then check after one to two days (section E). |
| Gemini CLI: Piebald-AI/awesome-gemini-cli-extensions | Pull request (README line) | Prepared. Waits for releases#49. | https://github.com/Piebald-AI/awesome-gemini-cli-extensions | Open the pull request after #49 merges (section E). |
| VS Code MCP gallery (`@mcp`) | GitHub MCP Registry, added by email after publishing to the official registry | Not listed (checked api.mcp.github.com: 394 curated servers, no LMCP). Prerequisite met. | https://github.com/mcp | Needs Dario: send the email in `SUBMISSIONS.md` section F to partnerships@github.com. |
| Windsurf (Devin Desktop) MCP marketplace | None documented. The marketplace uses a registry in the official MCP registry schema. | Not applicable for a submission. Cannot confirm whether LMCP appears. | https://docs.windsurf.com/windsurf/cascade/mcp | Needs Dario (2 minutes): open Devin Desktop, Cascade, MCP marketplace and search "local-mcp". If missing, ask Cognition support. Manual config already works (`mcp_config.json`). |
| Zed extensions | Zed is deprecating MCP-server extensions in favour of the official MCP Registry | Covered by the MCP Registry listing. No extension needed. | https://zed.dev/docs/extensions/mcp-extensions | None. Manual config is in the README (`context_servers`). |
| Goose extensions directory | Pull request to `documentation/static/servers.json` | Closed to new entries; Goose is integrating the official MCP Registry instead (discussion 10830). Covered by the MCP Registry listing. | https://github.com/aaif-goose/goose/discussions/10830 | None. Re-check if the directory reopens. |
| OpenCode | No MCP directory. Docs list community projects by pull request. | Not applicable. Manual config is in the README. | https://opencode.ai/docs/mcp-servers/ | None. |
| LM Studio | No catalog; "Add to LM Studio" deeplink | Prepared (deeplink in `SUBMISSIONS.md` section H) | https://lmstudio.ai/docs/app/mcp/deeplink | Add the button to the README install table in a follow-up after releases#49 merges. |
| Continue Hub | Hub login, "New block" | Prepared | https://hub.continue.dev | Needs Dario: publish the block (section G). |
| `npx skills` registry (skills.sh) | No submission; listed from install telemetry. Repo skills verified: `npx skills add colibird-ai/local-mcp-releases --list` shows 8 skills. | Installable, not yet ranked | https://www.skills.sh | Needs Dario (one command): `npx skills add colibird-ai/local-mcp-releases` once, so the first install is counted. |
| Docker MCP Catalog (docker/mcp-registry) | Pull request; local entries are containers, remote entries need test credentials | Not a fit for a local entry. Remote entry prepared but held. | https://github.com/docker/mcp-registry | Needs Dario: decide on the remote entry (section I). |
| Raycast | Raycast Store takes TypeScript extensions in raycast/extensions, not MCP servers | Not applicable | https://github.com/raycast/extensions | None. |
| mcpservers.org (wong2 list) | Web form, no login | Prepared | https://mcpservers.org/submit | Needs Dario or anyone on the team: submit (section J). |
| LobeHub MCP Marketplace | `lhm` CLI with browser login | Prepared (`listings/lobehub/lhm.plugin.json`) | https://lobehub.com/mcp | Needs Dario: login and GitHub connect (section K). |
| Awesome Claude Code | Human-written issue form only | Prepared, low probability | https://github.com/hesreallyhim/awesome-claude-code | Needs Dario after #3 merges (section L). |

## Merges and logins that unlock the most

1. colibird-ai/local-mcp-claude-plugin#3 and colibird-ai/local-mcp-releases#49: unlock Claude Code, Copilot CLI, Codex, Gemini CLI and Cursor installs, and the rows marked Prepared above.
2. Cursor form, Claude plugin directory form, GitHub MCP Registry email, Continue Hub block, LobeHub login, mcp.so and mcpservers.org forms.
