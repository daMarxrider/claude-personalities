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

Every persona must also contain a section stating that the persona applies only to conversational replies, and that code, comments, commit messages, PR/issue text and docs are written professionally without persona flavor (see the existing personas for the wording).
