# RunDrill Kazakh

Your personal **Kazakh coach** inside your AI agent — short targeted drills, an honest picture of
your level (A0–C2), and mistake memory that resurfaces what you got wrong. The skill is the voice;
your level, weak topics, vocabulary, and goal live on the RunDrill MCP server (`mcp.rundrill.com`),
synced across machines — not in a local file.

Built for real beginners: the course starts at **A0**, where many learners meet the Kazakh
Cyrillic alphabet (ә, ғ, қ, ң, ө, ұ, ү, һ, і) for the first time, and drills the things Kazakh
actually turns on — vowel harmony, agglutinated suffixes, and the cases — in plain language.

## One plugin, three hosts

The coaching skill (`skills/kazakh-coach/SKILL.md`) and `.mcp.json` are shared; each host reads its
own manifest and ignores the rest.

| Host | Reads |
|---|---|
| Claude Code / Claude Desktop | `.claude-plugin/plugin.json` + `.mcp.json` |
| OpenAI Codex | `.codex-plugin/plugin.json` + `.mcp.json` |
| Google Antigravity | `plugin.json` + `mcp_config.json` (+ `rules/`) |

On first use the host opens a browser tab for the OAuth handshake with `mcp.rundrill.com`, then
closes it — no API key to paste.

## Install

- **Claude Code / Desktop** — via the RunDrill marketplace:
  ```
  /plugin marketplace add rundrill/rundrill
  /plugin install rundrill-kazakh@rundrill
  ```
  Then run `/kazakh-coach`.
- **OpenAI Codex** — add the RunDrill catalog, then install `rundrill-kazakh` from the plugin directory:
  ```
  codex plugin marketplace add rundrill/rundrill
  ```
- **Google Antigravity** — drop this folder into `~/.gemini/config/plugins/rundrill-kazakh/` (global)
  or `<workspace>/.agents/plugins/rundrill-kazakh/` (workspace-scoped).

## License & attribution

© RunDrill. Licensed under **Creative Commons Attribution-NonCommercial-NoDerivatives 4.0
International (CC BY-NC-ND 4.0)** — full text in [LICENSE](LICENSE).

In short, you **may** view, run, and share this plugin unchanged, for non-commercial purposes, **as
long as you give credit**. You **may not**:

- use it, or any part of it (including the coaching skill), **commercially**;
- publish **modified or derivative** versions (forks, ports, translations, reworded skills).

Required attribution when sharing: *“RunDrill Kazakh coach — © RunDrill, CC BY-NC-ND 4.0,
https://rundrill.com”.*

For commercial use, derivatives, or any license beyond CC BY-NC-ND 4.0, contact
**salem@rundrill.com**.
