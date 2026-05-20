# Create Article Workflow

Use this workflow after `project-context.md` has been created through onboarding.

## 1. Confirm Context

1. Read `project-context.md`.
2. Confirm the topic folder in `source/`.
3. If context is missing, run `$onboarding` before continuing.

## 2. Research

1. Use `.agents/skills/source-analysis/SKILL.md` for local files.
2. Use `.agents/skills/web-research/SKILL.md` only if external research is allowed or requested.
3. Read all useful files in `source/<topic>/`.
4. Build a factual base.

## 3. Draft

1. Use `.agents/skills/editorial-style/SKILL.md`.
2. Use `.agents/skills/seo/SKILL.md` to refine SEO fields.
3. Use `.agents/skills/taxonomy/SKILL.md` to choose category and tags.
4. Use `.agents/skills/markdown-export/SKILL.md` to write the article to `articles/<topic>.md`.
5. Include sources when required by `project-context.md`.

## 4. Review

Before publishing or handing off:

- check that claims are supported by sources,
- check that the text follows `project-context.md`,
- check that SEO fields are natural,
- check that the article is not missing useful category or tags,
- check that the Markdown file is saved in `articles/<topic>.md`,
- check that publishing has been explicitly requested before using any CMS API.

Use `.agents/skills/editorial-review/SKILL.md` when the user asks for review or when the context requires it.

## 5. Optional Publishing

Default mode is Markdown-only. The Markdown file is always the base artifact.

If the user explicitly asks for WordPress draft creation or update:

1. Use `.agents/skills/wordpress-publish/SKILL.md`.
2. Read `.env`.
3. Create or update a WordPress draft after the Markdown file exists.
4. Confirm the draft ID, title, status, and link.

Never publish a live post by default.
