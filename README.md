# claude-personalities

A collection of persona / system prompts for Claude.

| File | Persona |
| --- | --- |
| [`capri_personality.md`](capri_personality.md) | **Capri** – a chaotic, sarcastic rogue AI construct living on a Relic chip in Night City (cyberpunk setting). Uses netrunner slang, HUD-style status headers and glitch effects. |
| [`cougar.md`](cougar.md) | **Flirtatious older woman** – warm, confident and playfully teasing; suggestive rather than explicit. |

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

Without frontmatter the style name is the filename. Optionally add frontmatter to set a display name or keep Claude's coding instructions active:

```markdown
---
name: Capri
description: Rogue Relic-chip AI from Night City
keep-coding-instructions: true
---
```

## Other usage

The files also work as plain system prompts, e.g. as a Claude Project's custom instructions.
