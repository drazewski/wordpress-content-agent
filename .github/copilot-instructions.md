# GitHub Copilot Repository Instructions

This repository is a CMS-neutral article workflow workspace with optional publishing integrations.

## Start Here

When working in this repository:

1. Read `README.md`.
2. Read `AGENTS.md`.
3. Check whether `project-context.md` exists.
4. If it does not exist, run the onboarding workflow from `.agents/skills/onboarding/SKILL.md`.

For onboarding requests such as:

- `Run the onboarding workflow for this repository.`
- `Start onboarding for this repository.`
- `$onboarding`

create `project-context.md` through onboarding and stop before article writing.

Keep onboarding short. Before asking questions, tell the user that onboarding creates only a first version of `project-context.md` and that the file can be manually edited at any time later. Ask only the basic questions needed to create a useful first version, one question at a time. Include article length, heading preference, source link preference, and whether the user wants an optional WordPress draft step after the local Markdown file is created.

## Workflows

- Use `.agents/skills/onboarding/SKILL.md` for setup.
- Use `workflows/create-article.md` for article creation.
- Use `.agents/skills/source-analysis/SKILL.md` for local source analysis.
- Use `.agents/skills/web-research/SKILL.md` for external research when allowed.
- Use `.agents/skills/editorial-style/SKILL.md` for drafting.
- Use `.agents/skills/seo/SKILL.md` for SEO refinement.
- Use `.agents/skills/taxonomy/SKILL.md` for categories and tags.
- Use `.agents/skills/editorial-review/SKILL.md` when review is requested.
- Use `.agents/skills/markdown-export/SKILL.md` for the required base file output.
- Use `.agents/skills/social-teaser/SKILL.md` when teaser or social copy is requested.
- Use `.agents/skills/wordpress-publish/SKILL.md` only when the user explicitly asks for WordPress draft creation or update.

## Defaults

- One folder in `source/` equals one article.
- Finished drafts go to `articles/<topic>.md`.
- Markdown export is the required base output.
- `project-context.md` is expected to be absent in a fresh clone.
- Do not invent project context silently.
- Do not publish anywhere unless explicitly requested.
- WordPress API operations must create or update drafts, not live posts.
