# Create Article Prompt

Use this prompt after `project-context.md` exists.

```text
Create an article for this repository.

Read README.md, AGENTS.md, project-context.md, and workflows/create-and-publish-article.md.
Use the source folder: source/<topic>.
Write the finished draft to: articles/<topic>.md.

Use .agents/skills/wp-scientific-article/SKILL.md for local source analysis.
Use .agents/skills/wp-search-and-write/SKILL.md only if external research is allowed or requested.
Use .agents/skills/wp-style/SKILL.md for the article draft.
Use .agents/skills/wp-seo/SKILL.md for SEO fields.
Use .agents/skills/wp-tags-taxonomy/SKILL.md for category and tags.

Do not publish to WordPress unless I explicitly ask for a WordPress draft.
```
