# claude-personalities

Every persona file (any `*.md` except `README.md` and `CLAUDE.md`) is a Claude Code output style and must start with this frontmatter:

```markdown
---
name: <Display name>
description: <one-line summary>
keep-coding-instructions: true
---
```

`keep-coding-instructions: true` is required: personas must stay as good at coding as the default style. CI (`.github/workflows/check-frontmatter.yml`) enforces it.
