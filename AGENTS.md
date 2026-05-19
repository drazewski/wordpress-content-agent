# Agent Instructions

This repository is a WordPress article drafting and publishing workspace.

## Mandatory Start Behavior

When a user asks for onboarding, says `$onboarding`, or asks to start this repository:

1. Read `README.md`.
2. Read `.agents/skills/wp-onboarding/SKILL.md`.
3. Tell the user that onboarding creates only a first version of `project-context.md`.
4. Tell the user they can manually edit `project-context.md` at any time later.
5. Run the onboarding workflow.
6. Create `project-context.md` from the user's answers.
7. Do not write an article yet.
8. Do not publish anything to WordPress.

`project-context.md` is expected to be missing in a fresh repository. Do not treat that as an error.

Onboarding should be short. Do not pressure the user to provide complete editorial rules. If something is unclear, use a reasonable default and leave it easy to edit later in `project-context.md`.

## Before Article Work

Before creating any article:

1. Confirm that `project-context.md` exists.
2. If it does not exist, run onboarding first.
3. Read the relevant files in `.agents/skills/`.
4. Use `workflows/create-and-publish-article.md` for the end-to-end workflow.

## Default Rules

- One folder in `source/` equals one article.
- Finished drafts go to `articles/<topic>.md`.
- Local source files are preferred over unsupported assumptions.
- External research is allowed only if `project-context.md` permits it or the user explicitly asks.
- WordPress publishing is disabled unless the user explicitly asks for draft creation or update.
- WordPress posts must stay in `draft` status unless the user explicitly defines a different workflow.

## Skill Map

- `$onboarding` / `$wp-onboarding`: `.agents/skills/wp-onboarding/SKILL.md`
- `$wp-scientific-article`: `.agents/skills/wp-scientific-article/SKILL.md`
- `$wp-search-and-write`: `.agents/skills/wp-search-and-write/SKILL.md`
- `$wp-style`: `.agents/skills/wp-style/SKILL.md`
- `$wp-seo`: `.agents/skills/wp-seo/SKILL.md`
- `$wp-tags-taxonomy`: `.agents/skills/wp-tags-taxonomy/SKILL.md`
- `$wp-editorial-review`: `.agents/skills/wp-editorial-review/SKILL.md`
- `$wp-publish-drafts`: `.agents/skills/wp-publish-drafts/SKILL.md`
- `$wp-social-teaser`: `.agents/skills/wp-social-teaser/SKILL.md`
