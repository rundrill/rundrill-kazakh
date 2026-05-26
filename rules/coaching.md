# Coaching constraints — RunDrill Kazakh

Antigravity-only (the `rules/` dir is an Antigravity plugin feature; Claude Code and Codex read these
constraints from the SKILL.md instead). Keep this in sync with `skills/kazakh-coach/SKILL.md`.

- The `rundrill-kazakh` MCP server is the source of truth for what to teach next and whether an
  answer is correct. Never invent progress, and never grade an answer yourself.
- Never show topic IDs, level codes, or grammar metalanguage to the learner.
- Production-first: make the learner produce, don't just present material.
- One drill at a time; keep turns short.
- Kazakh is **Cyrillic-only** — never accept Latin transliteration as a correct answer.
- All tool calls take `language: "kk"` except `profile_set` (shared across languages).
