# OpenAI plugin directory package

Source of the ZIP uploaded to https://platform.openai.com/plugins for the plugin "LMCP" (shared by ChatGPT and Codex). The ZIP is built from this folder plus files that already live in the repository:

```
.codex-plugin/plugin.json   # this folder
.mcp.json                   # this folder: the hosted MCP server
assets/logo.png             # repository root: assets/logo.png (512x512)
skills/<six skills>/        # repository root: skills/
```

Skills in the package: `local-mcp-daily-brief`, `local-mcp-email-to-action`, `local-mcp-pdf-to-sheet`, `local-mcp-calendar`, `local-mcp-email`, `local-mcp-files`. `local-mcp-messages` and `local-mcp-teamchat` are left out on purpose: version 1.0.0 was rejected for relaying third-party integrations.

## Build

```bash
d=$(mktemp -d) && cp -R listings/openai/.codex-plugin listings/openai/.mcp.json "$d"/ \
  && mkdir -p "$d/assets" "$d/skills" && cp assets/logo.png "$d/assets/" \
  && for s in daily-brief email-to-action pdf-to-sheet calendar email files; do cp -R "skills/local-mcp-$s" "$d/skills/"; done \
  && (cd "$d" && zip -q -r -X lmcp-openai.zip .codex-plugin .mcp.json assets skills) && echo "$d/lmcp-openai.zip"
```

## What the portal checks on upload (learned on 2026-10-09)

- Bump `version` in `plugin.json` on every upload; `name` stays `app-6a2f301f84bc8191bf18c5c73b1594a4` (the existing plugin).
- The package must declare the plugin's existing MCP (`mcpServers` → `.mcp.json`, same URL). Without it: "This package omits the plugin's existing MCP". The ZIP that "Download release ZIP" returns does not include that declaration, nor the icon or skills.
- An icon is required (`interface.logo` / `interface.composerIcon`).
- Only one review can be active: "Cancel review" before uploading a new version.
- Test cases, reviewer credentials and the demo video are kept in the dashboard for this plugin, not in the ZIP.
- "Submit for review" asks the developer to tick six legal attestations; the account owner does that.
