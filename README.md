# WordPress Content Agent

Start here.

This repository is a reusable workspace for creating WordPress article drafts with AI agents such as Codex, GitHub Copilot, Claude, Gemini, or similar tools.

The first action in a fresh copy of this repository is always onboarding.

`project-context.md` is intentionally not included. It must be created by the onboarding workflow for the specific site, author, brand, or editorial team.

Onboarding is intentionally short. It creates a first usable `project-context.md`, and you can manually edit that file at any time later.

## You Can Edit Context Later

The onboarding result is not final or locked. It is only a starting profile for the agent.

After onboarding, you can open `project-context.md` and change anything manually:

- site description,
- tone,
- source rules,
- categories and tags,
- WordPress publishing mode,
- notes about what to avoid,
- examples of articles to follow.

You do not need to get everything right during onboarding.

## Start Onboarding

Use any of these entry points:

```text
codex "Start onboarding for this repository"
```

```text
codex "$onboarding"
```

In GitHub Copilot:

```text
Run the onboarding workflow for this repository.
```

Or copy the ready prompt from:

```text
prompts/start-onboarding.md
```

The agent should:

1. Read `README.md`.
2. Read `AGENTS.md`.
3. Read `.agents/skills/wp-onboarding/SKILL.md`.
4. Tell the user that `project-context.md` can be edited manually later.
5. Ask only short onboarding questions.
6. Create `project-context.md`.
7. Stop before article writing or WordPress publishing.

## Create An Article

After onboarding:

1. Create one topic folder in `source/`.
   - Example: `source/mikroplastik-w-rzekach/`
2. Add all source materials for one article to that folder.
   - PDFs, reports, notes, links, briefs, text files, and reference material are all acceptable.
3. Ask the agent to create the article, or copy:

```text
prompts/create-article.md
```

Finished drafts should be written to:

```text
articles/<topic>.md
```

## Repository Layout

```text
.
+-- AGENTS.md
+-- README.md
+-- .agents/
|   +-- skills/
|       +-- wp-onboarding/
|       |   +-- SKILL.md
|       +-- wp-scientific-article/
|       |   +-- SKILL.md
|       +-- wp-search-and-write/
|       |   +-- SKILL.md
|       +-- wp-style/
|       |   +-- SKILL.md
|       +-- wp-seo/
|       |   +-- SKILL.md
|       +-- wp-tags-taxonomy/
|       |   +-- SKILL.md
|       +-- wp-publish-drafts/
|       |   +-- SKILL.md
|       +-- wp-social-teaser/
|       |   +-- SKILL.md
|       +-- wp-editorial-review/
|           +-- SKILL.md
+-- .github/
|   +-- copilot-instructions.md
|   +-- instructions/
|       +-- wordpress-publisher.instructions.md
+-- workflows/
|   +-- create-and-publish-article.md
+-- prompts/
|   +-- start-onboarding.md
|   +-- create-article.md
+-- source/
+-- articles/
+-- .env.example
```

## Agent Workflow

Agents should use the repository in this order:

1. `wp-onboarding` - create or refresh `project-context.md`.
2. `wp-scientific-article` - analyze PDFs, reports, and local source documents.
3. `wp-search-and-write` - use external research only when allowed or requested.
4. `wp-style` - draft the article in the configured editorial style.
5. `wp-seo` - refine title, slug, excerpt, and meta description.
6. `wp-tags-taxonomy` - choose category and tags.
7. `wp-editorial-review` - optional review before publication.
8. `wp-publish-drafts` - create or update a WordPress draft only when explicitly requested.
9. `wp-social-teaser` - optional teaser/social copy.

For a complete article workflow, read:

```text
workflows/create-and-publish-article.md
```

## WordPress Publishing

Default mode is file-only. Agents must not publish or update WordPress drafts unless the user explicitly asks.

To enable WordPress draft creation:

1. Copy `.env.example` to `.env`.
2. Fill in the WordPress API settings.
3. Ask the agent to create or update a draft.

The default WordPress status is always `draft`.
