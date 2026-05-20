# Create Article Prompt

Use this prompt after `project-context.md` exists.

```text
Create an article for this repository.

Read README.md, AGENTS.md, project-context.md, and workflows/create-article.md.
Use the source folder: source/<topic>.
Write the finished draft to: articles/<topic>.md.

Use .agents/skills/source-analysis/SKILL.md for local source analysis.
Use .agents/skills/web-research/SKILL.md only if external research is allowed or requested.
Use .agents/skills/editorial-style/SKILL.md for the article draft.
Use .agents/skills/seo/SKILL.md for SEO fields.
Use .agents/skills/taxonomy/SKILL.md for category and tags.
Use .agents/skills/markdown-export/SKILL.md to save the final file.

Always create the Markdown file first.
Do not publish anywhere unless I explicitly ask for an additional publishing integration.
```
