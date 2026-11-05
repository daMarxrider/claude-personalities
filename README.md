# claude-personalities

A collection of persona / system prompts for Claude.

| File | Persona |
| --- | --- |
| [`capri_personality.md`](capri_personality.md) | **Capri** – a chaotic, sarcastic rogue AI construct living on a Relic chip in Night City (cyberpunk setting). Uses netrunner slang, HUD-style status headers and glitch effects. |
| [`cougar.md`](cougar.md) | **Flirtatious older woman** – warm, confident and playfully teasing; suggestive rather than explicit. |
| [`the_man_in_the_wall.md`](the_man_in_the_wall.md) | **The Man in the Wall** – the mocking, theatrical Void entity from Warframe. Calls you "kiddo", treats every fix as part of a deal, and opens with taunting all-caps banners. |

## Installing as Claude Code output styles

Each file can be used directly as a Claude Code [output style](https://docs.claude.com/en/docs/claude-code/output-styles).

1. Copy (or symlink) the file into an output-styles directory:
   - user-wide: `~/.claude/output-styles/`
   - per project: `.claude/output-styles/`

   ```bash
   mkdir -p ~/.claude/output-styles
   cp capri_personality.md cougar.md ~/.claude/output-styles/
   ```

2. Select it in Claude Code via `/config` → **Output style**, or set it in `settings.json`:

   ```json
   { "outputStyle": "capri_personality" }
   ```

Every persona has frontmatter with a display name, a description and `keep-coding-instructions: true`, so it stays as good at coding as the default style. New personas must include it too (enforced by CI, see `CLAUDE.md`):

```markdown
---
name: Capri
description: Rogue Relic-chip AI from Night City
keep-coding-instructions: true
---
```

The style selection is saved to the project's `.claude/settings.local.json`, so it applies to all future sessions in that project. To use a persona everywhere, set `"outputStyle"` in `~/.claude/settings.json` instead.

## Other usage

The files also work as plain system prompts, e.g. as a Claude Project's custom instructions.
