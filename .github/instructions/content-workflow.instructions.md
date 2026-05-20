---
applyTo: "**/*"
---

# Content Workflow Instructions

This repository supports article drafting with optional publishing integrations.

Before article work, confirm that `project-context.md` exists. If it does not exist, run onboarding from `.agents/skills/onboarding/SKILL.md`.

Use the repository workflow:

1. Read `project-context.md`.
2. Read `workflows/create-article.md`.
3. Use `source/<topic>/` as the input folder.
4. Use `.agents/skills/markdown-export/SKILL.md` to write finished drafts to `articles/<topic>.md`.
5. Use publishing integrations only after the Markdown file exists and only when the user explicitly asks.

WordPress publishing constraints:

- Use `.agents/skills/wordpress-publish/SKILL.md`.
- Read credentials from `.env`.
- Default status is `draft`.
- Never publish live posts by default.
- Report WordPress API errors clearly.
