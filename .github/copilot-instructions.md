# GitHub Copilot Repository Instructions

This repository is a WordPress article drafting and draft-publishing workspace.

## Start Here

When working in this repository:

1. Read `README.md`.
2. Read `AGENTS.md`.
3. Check whether `project-context.md` exists.
4. If it does not exist, run the onboarding workflow from `.agents/skills/wp-onboarding/SKILL.md`.

For onboarding requests such as:

- `Run the onboarding workflow for this repository.`
- `Start onboarding for this repository.`
- `$onboarding`

create `project-context.md` through onboarding and stop before article writing.

Keep onboarding short. Before asking questions, tell the user that onboarding creates only a first version of `project-context.md` and that the file can be manually edited at any time later. Ask only the basic questions needed to create a useful first version.

## Workflows

- Use `.agents/skills/wp-onboarding/SKILL.md` for setup.
- Use `workflows/create-and-publish-article.md` for article creation.
- Use `.agents/skills/wp-scientific-article/SKILL.md` for local source analysis.
- Use `.agents/skills/wp-search-and-write/SKILL.md` for external research when allowed.
- Use `.agents/skills/wp-style/SKILL.md` for drafting.
- Use `.agents/skills/wp-seo/SKILL.md` for SEO refinement.
- Use `.agents/skills/wp-tags-taxonomy/SKILL.md` for categories and tags.
- Use `.agents/skills/wp-editorial-review/SKILL.md` when review is requested.
- Use `.agents/skills/wp-publish-drafts/SKILL.md` only when the user explicitly asks for WordPress draft creation or update.

## Defaults

- One folder in `source/` equals one article.
- Finished drafts go to `articles/<topic>.md`.
- `project-context.md` is expected to be absent in a fresh clone.
- Do not invent project context silently.
- Do not publish to WordPress unless explicitly requested.
- WordPress API operations must create or update drafts, not live posts.
