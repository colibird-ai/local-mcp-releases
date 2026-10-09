# Prepared submissions

Ready-to-paste payloads for the channels in `STATUS.md` that need a form, an account login or a merge first. Copy comes from `DESCRIPTIONS.md`. Every submission is made by the LMCP team (Colibird).

## Order of operations

1. Merge colibird-ai/local-mcp-claude-plugin#3 (Claude Code marketplace, Copilot CLI marketplace, accurate plugin metadata).
2. Merge colibird-ai/local-mcp-releases#49 (Codex plugin, Gemini CLI extension, install section) and then the PR that carries this folder.
3. Tag the plugin repository so reviewers can pin a ref:
   `gh release create v1.2.0 -R colibird-ai/local-mcp-claude-plugin --target main --title "v1.2.0" --notes "Claude Code and Copilot CLI plugin for LMCP"` (use the version in `.claude-plugin/plugin.json` after #3 merges).
4. Run the forms and logins below. Items 1 to 3 unlock A, B, C, D and E.

## A. Claude plugin directory (Anthropic, official)

- Form: https://clau.de/plugin-directory-submission (source: README of https://github.com/anthropics/claude-plugins-official, section "External Plugins")
- Plugin repository: https://github.com/colibird-ai/local-mcp-claude-plugin
- Plugin name: `local-mcp`; marketplace entry name in the same repository: `local-mcp`
- Description: short description from `DESCRIPTIONS.md`
- Homepage: https://www.local-mcp.com; Privacy: https://www.local-mcp.com/en/privacy; Contact: ctpo@colibird.co
- Needs: Dario fills the form (it asks for a contact identity). Requires #3 merged.

## B. Cursor Marketplace

- Form: https://cursor.com/marketplace/publish (submit the repository link; every plugin is reviewed manually and must be open source)
- Repository: https://github.com/colibird-ai/local-mcp-releases
- Manifest on `main`: `.cursor-plugin/plugin.json` (name `local-mcp`, logo `assets/logo.png`); also ships `mcp.json`, `rules/local-mcp.mdc` and `skills/`.
- Checked on 2026-10-08: https://cursor.com/marketplace/local-mcp returns "Marketplace Plugin Not Found". LMCP is not listed.
- Risk to state if asked: the repository mixes MIT documentation and plugin files with a proprietary app binary. The plugin files themselves (manifest, `mcp.json`, rule, skills) are MIT; say so in the form notes.
- Needs: Dario's Cursor account.

## C. GitHub Copilot plugins

- `github/copilot-plugins`: pull request opened from the `lanchuske` fork (see `STATUS.md` for the link). Third-party pull requests in that repository have not been merged so far; no further action is needed from us.
- `github/awesome-copilot` (community collection; external plugins go through an issue form, not a pull request):
  - Issue form: https://github.com/github/awesome-copilot/issues/new?template=external-plugin.yml
  - Title: `[External Plugin]: local-mcp`
  - Plugin name: `local-mcp`
  - Short description: short description from `DESCRIPTIONS.md`
  - GitHub repository: `colibird-ai/local-mcp-claude-plugin`
  - Plugin path: leave empty (repository root)
  - Ref to review: the release tag from step 3 (for example `v1.1.0`)
  - Commit SHA to review: `gh api repos/colibird-ai/local-mcp-claude-plugin/commits/v1.1.0 --jq .sha` (full 40 characters)
  - Version: the version in `.claude-plugin/plugin.json`
  - License: `MIT`
  - Author name: `LMCP`; Author URL: `https://www.local-mcp.com`; Homepage: `https://www.local-mcp.com`
  - Keywords: `mcp, mail, calendar, contacts, teams, slack, whatsapp, onedrive, google-drive, notion, outlook, office, macos, windows, productivity`
  - Notes for reviewers: "Submitted by the LMCP team. The plugin starts the LMCP MCP server (`npx -y local-mcp@latest`); the LMCP app must be installed first. Also listed in the official MCP Registry as com.local-mcp/local-mcp."
  - Tick all four checkboxes. After the bot labels it, `/rerun-intake` re-runs the checks.
  - Needs #3 merged and the tag. The issue form can be filed from the `lanchuske` account.

## D. Codex

- **Submitted.** Status and history are in `STATUS.md`; the package source and the build steps are in `listings/openai/README.md`. The requirements below are kept for reference.
- Official OpenAI plugin directory (shared by ChatGPT and Codex): portal https://platform.openai.com/plugins (guide: https://developers.openai.com/plugins/deploy/submission). Needs an organization owner or "Apps Management Write", a verified developer identity, a ZIP of the plugin, domain verification for the hosted MCP server, five positive and three negative test cases, reviewer credentials and a demo video. Manifest limits: `displayName` 30 characters or fewer (`LMCP`), `shortDescription` 30 characters or fewer (use the tagline), `longDescription` 4000 characters or fewer (long description from `DESCRIPTIONS.md`), plus `websiteURL`, `supportURL`, `privacyPolicyURL`, `termsOfServiceURL`. Needs Dario and a deliberate decision: the hosted connector only answers tools after the LMCP app is installed.
- Community list `hashgraph-online/awesome-codex-plugins`: one README line, after #49 merges and after the HOL scanner score is 80/130 or higher with no high findings (`pipx install "plugin-scanner==3.32.0"` then `plugin-scanner scan . --format text`). It also asks for `SECURITY.md` (present), `LICENSE`, `README.md` and a dependency lockfile (not present). Line:
  `- [LMCP](https://github.com/colibird-ai/local-mcp-releases) - Local tools that let Codex use Mail, Calendar, Contacts, Teams, Slack, WhatsApp (Mac), OneDrive, Google Drive, Notion, Outlook (Windows) and Office files on Mac and Windows.`

## E. Gemini CLI

- Extensions gallery (https://geminicli.com/extensions) is a daily crawl; there is no form. Requirements: public GitHub repository, topic `gemini-cli-extension` (already set), `gemini-extension.json` at the repository root (arrives with #49). Check after one to two days: `curl -s https://geminicli.com/extensions.json | grep -c local-mcp`. If it is missing after four daily crawls, open a "GeminiCLI.com Feedback" issue in google-gemini/gemini-cli (precedents: issues 28861 and 29623).
- Community list `Piebald-AI/awesome-gemini-cli-extensions`: README line at the bottom of the matching section, after #49 merges:
  `- [**LMCP**](https://github.com/colibird-ai/local-mcp-releases) - Local tools that let Gemini CLI use Mail, Calendar, Contacts, Teams, Slack, WhatsApp (Mac), OneDrive, Google Drive, Notion, Outlook (Windows) and Office files on Mac and Windows.`

## F. GitHub MCP Registry (this is what VS Code's `@mcp` gallery shows)

- Checked on 2026-10-08: the registry (api.mcp.github.com, 394 curated servers) does not contain LMCP. VS Code reads this registry, so LMCP is absent from the gallery.
- LMCP is already published in the official MCP Registry (`com.local-mcp/local-mcp`, active), which is the prerequisite. GitHub then adds servers by email.
- Email to: partnerships@github.com
- Subject: `Request to include com.local-mcp/local-mcp in the GitHub MCP Registry`
- Body:
  > Hello, we are the LMCP team (Colibird). Please include our MCP server in the GitHub MCP Registry so it appears in VS Code's MCP gallery.
  >
  > Official MCP Registry name: com.local-mcp/local-mcp.
  > Repository: https://github.com/colibird-ai/local-mcp-releases
  > Website: https://www.local-mcp.com
  >
  > Local tools that let your AI use Mail, Calendar, Contacts, Teams, Slack, WhatsApp (Mac), OneDrive, Google Drive, Notion, Outlook (Windows) and Office files on Mac and Windows. Runs on your computer.
  >
  > Contact: ctpo@colibird.co
- Needs: Dario sends it (or approves sending it from his mailbox).

## G. Continue Hub

- Where: https://hub.continue.dev, "New block", type "MCP server" (login with Dario's Continue account; the owner slug will be his or an organization's).
- Block file:

```yaml
name: LMCP
version: latest
schema: v1
mcpServers:
  - name: LMCP
    command: npx
    args:
      - "-y"
      - "local-mcp@latest"
```

- Block description: short description from `DESCRIPTIONS.md`. Icon: `assets/logo.png`. Website: https://www.local-mcp.com.
- Users can also drop the same file into `.continue/mcpServers/local-mcp.yaml` without the hub.

## H. LM Studio

- There is no catalog to submit to. LM Studio (0.3.17 and later) installs MCP servers from a deeplink. Button for README, docs and the website:
  `[![Add to LM Studio](https://files.lmstudio.ai/deeplink/mcp-install-light.svg)](lmstudio://add_mcp?name=local-mcp&config=eyJjb21tYW5kIjoibnB4IiwiYXJncyI6WyIteSIsImxvY2FsLW1jcEBsYXRlc3QiXX0%3D)`
- Decoded config: `{"command":"npx","args":["-y","local-mcp@latest"]}`
- Suggested placement: the `Cline, LM Studio, Continue, Goose, OpenCode` row of the install table in the main README and the web guide, in a follow-up after #49 merges (not done here to avoid conflicting with that pull request).

## I. Docker MCP Catalog (docker/mcp-registry)

- Local entries must be a container built from a Dockerfile in an open-source repository (MIT or Apache 2 preferred). LMCP runs natively against macOS and Windows apps and is proprietary, so a local entry is not possible.
- A remote entry is possible, but the remote endpoint only returns real tools after the user has installed the LMCP app and turned on Cloud Data Forwarding, and Docker asks for test credentials through a form. Decision for Dario; do not submit until he confirms. If he does, `task remote-wizard` creates `servers/local-mcp/` with:

```yaml
name: local-mcp
type: remote
dynamic:
  tools: true
meta:
  category: productivity
  tags:
    - productivity
    - remote
    - macos
    - windows
about:
  title: LMCP
  description: Local tools that let your AI use Mail, Calendar, Contacts, Teams, Slack, WhatsApp (Mac), OneDrive, Google Drive, Notion, Outlook (Windows) and Office files on Mac and Windows. Requires the LMCP app and Cloud Data Forwarding.
  icon: https://www.local-mcp.com/icon-400.png
remote:
  transport_type: streamable-http
  url: https://www.local-mcp.com/mcp
oauth:
  - provider: local-mcp
    secret: local-mcp.personal_access_token
    env: LOCAL_MCP_PERSONAL_ACCESS_TOKEN
```

  plus `tools.json` containing `[]` and `readme.md` linking https://github.com/colibird-ai/local-mcp-releases/blob/main/llms-install.md. Test credentials: https://forms.gle/6Lw3nsvu2d6nFg8e6

## J. mcpservers.org (feeds the wong2 awesome list)

- Form (no login, review within two weeks): https://mcpservers.org/submit
- Server name: `LMCP`; Category: `Productivity`; Short description: short description from `DESCRIPTIONS.md`; Repository, website or documentation: https://github.com/colibird-ai/local-mcp-releases; Official MCP Registry name: `com.local-mcp/local-mcp`; tick "This server supports remote connections"; Contact email: ctpo@colibird.co; plan: Free.

## K. LobeHub MCP Marketplace

- Self-service CLI, needs Dario's browser for `login` and `github connect` (guide: https://lobehub.com/publish-mcp/skill.md). Commands:
  `npx -y @lobehub/market-cli login`, `npx -y @lobehub/market-cli github connect`, then from the folder with `lhm.plugin.json` (see `listings/lobehub/lhm.plugin.json`):
  `npx -y @lobehub/market-cli plugin publish https://github.com/colibird-ai/local-mcp-releases --dir "$(pwd)/listings/lobehub"`
- Earlier requests lobehub/lobehub#13354 and #16263 are closed; the CLI is the supported path.
- Published 2026-10-09. Later versions: bump `version` in `lhm.plugin.json` and run `npx -y @lobehub/market-cli plugin update --dir "$(pwd)/listings/lobehub"`; `plugin publish` refuses an existing listing.

## L. Awesome Claude Code

- `hesreallyhim/awesome-claude-code` accepts recommendations only through its web issue form, written by a human, and says closed-source projects and anything that needs a sign-up are hard to review. Rules: at least 14 days of history with continued commits, or 100 stars; one resource at a time; one-line description, no emojis, no sales language.
- Form: https://github.com/hesreallyhim/awesome-claude-code/issues/new?template=recommend-resource.yml
- Resource: https://github.com/colibird-ai/local-mcp-claude-plugin ; description: `Plugin and marketplace that connect Claude Code to local Mail, Calendar, Contacts, Teams, Slack, WhatsApp (Mac), OneDrive, Google Drive, Notion, Outlook (Windows) and Office files on Mac and Windows.`
- Low probability. Submit after #3 is merged and there are community adoption signals.

## M. Awesome AI Plugins (HOL)

- Community list `hashgraph-online/awesome-ai-plugins` (same organization as the Codex list in section D; about 495 stars, merges within hours, last commit the day it was checked). The maintainers invited the listing in local-mcp-releases#48. Rules (`CONTRIBUTING.md`): one README line, alphabetical order inside the section (`python3 scripts/check-alphabetical.py`), one sentence, search first. The catalog runs its own required source scan (80 or higher, no critical or high findings); scanner CI in our repository is optional.
- Section: Community Plugins > Tools & Integrations, between LinkMCP and Logo Design Skill. Line:
  `- [LMCP](https://github.com/colibird-ai/local-mcp-releases) - Local MCP server and plugins that let an assistant use Mail, Calendar, Contacts, Teams, Slack, WhatsApp (Mac), OneDrive, Google Drive, Notion, Outlook (Windows) and Office files on macOS and Windows.`
- Done 2026-10-08: pull request https://github.com/hashgraph-online/awesome-ai-plugins/pull/666 from the `lanchuske` fork. No pricing words in the line (see the rules in `DESCRIPTIONS.md`).
- After the merge the bot comments a claim link (as it did on awesome-codex-plugins#499): the GitHub account that maintains the repository can open it and continue with GitHub to claim the listing. That step is Dario's.
