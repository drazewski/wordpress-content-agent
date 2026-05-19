---
applyTo: "**/*"
---

# WordPress Publisher Instructions

This repository supports WordPress article drafting with optional draft publishing.

Before article work, confirm that `project-context.md` exists. If it does not exist, run onboarding from `.agents/skills/wp-onboarding/SKILL.md`.

Use the repository workflow:

1. Read `project-context.md`.
2. Read `workflows/create-and-publish-article.md`.
3. Use `source/<topic>/` as the input folder.
4. Write finished drafts to `articles/<topic>.md`.
5. Use WordPress publishing only when the user explicitly asks.

Publishing constraints:

- Use `.agents/skills/wp-publish-drafts/SKILL.md`.
- Read credentials from `.env`.
- Default status is `draft`.
- Never publish live posts by default.
- Report WordPress API errors clearly.
