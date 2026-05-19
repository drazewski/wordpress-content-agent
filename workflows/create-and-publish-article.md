# Create And Publish Article Workflow

Use this workflow after `project-context.md` has been created through onboarding.

## 1. Confirm Context

1. Read `project-context.md`.
2. Confirm the topic folder in `source/`.
3. If context is missing, run `$onboarding` before continuing.

## 2. Research

1. Use `.agents/skills/wp-scientific-article/SKILL.md` for local files.
2. Use `.agents/skills/wp-search-and-write/SKILL.md` only if external research is allowed or requested.
3. Read all useful files in `source/<topic>/`.
4. Build a factual base.

## 3. Draft

1. Use `.agents/skills/wp-style/SKILL.md`.
2. Write the article to `articles/<topic>.md`.
3. Include front matter with title, excerpt, slug, tags, category, and meta description.
4. Include sources when required by `project-context.md`.
5. Use `.agents/skills/wp-seo/SKILL.md` to refine SEO fields.
6. Use `.agents/skills/wp-tags-taxonomy/SKILL.md` to choose category and tags.

## 4. Review

Before publishing or handing off:

- check that claims are supported by sources,
- check that the text follows `project-context.md`,
- check that SEO fields are natural,
- check that the article is not missing category or tags,
- check that WordPress publishing has been explicitly requested before using the API.

## 5. Publish Draft Only When Requested

If the user explicitly asks for WordPress draft creation or update:

1. Use `.agents/skills/wp-publish-drafts/SKILL.md`.
2. Read `.env`.
3. Create or update a WordPress draft.
4. Confirm the draft ID, title, status, and link.

Never publish a live post by default.
