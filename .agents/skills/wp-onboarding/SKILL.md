---
name: wp-onboarding
description: Quickly create project-context.md for a WordPress content workflow before article creation starts.
aliases:
  - onboarding
  - $onboarding
---

# Purpose

Use this skill first in every fresh copy of the repository.

The goal is not to collect a perfect editorial manual. The goal is to create a useful first version of `project-context.md` quickly, so the user can start creating articles.

At the beginning of onboarding, tell the user:

```text
This onboarding will stay short. I will create the first version of project-context.md from your answers. You can manually edit that file at any time later, so you do not need to provide perfect or complete answers now.
```

# First-run rules

- Keep onboarding short.
- Ask only the minimum questions needed to avoid bad assumptions.
- Prefer multiple-choice style suggestions and defaults.
- Remind the user that missing details can be added later by editing `project-context.md`.
- Do not ask for long lists, detailed style rules, examples, or phrases to avoid during first onboarding.
- If the user gives a vague answer, use a reasonable default and mark it as a default in `project-context.md`.
- Do not start article writing during onboarding.
- Do not publish anything to WordPress.

# Minimum questions

Ask these questions in one or two small batches.

## Batch 1: editorial basics

1. What is the site or project about?
2. Who is the main reader?
3. What kind of articles should the agent usually create?
   - suggested choices: guides, news, research summaries, analyses, reviews, opinion/commentary
4. What tone should the articles use?
   - suggested choices: factual, approachable, expert, conversational, formal

## Batch 2: workflow basics

5. Where will article material usually come from?
   - suggested choices: local files in `source/`, user-provided links, web research, mixed
6. Can the agent use external web research when local material is not enough?
   - suggested choices: yes, only after asking, no
7. Should finished articles stay as files, or can the agent create WordPress drafts?
   - suggested choices: files only, WordPress drafts after approval
8. Do you already have fixed WordPress categories or tags?
   - suggested choices: no, yes and I will provide them later, yes and I will provide them now

# Optional follow-up only if needed

Ask these only when the user's earlier answers make them necessary:

- What language should the articles be written in?
- Should articles include a source list?
- Is there a strict maximum or preferred article length?
- Is there a specific WordPress API/proxy setup already available?

# Do not ask during first onboarding

Do not ask these during first onboarding unless the user volunteers the information:

- long lists of phrases or words to avoid,
- detailed heading rules,
- reference articles to emulate,
- detailed SEO strategy,
- internal linking strategy,
- social media teaser requirements,
- comparison against an existing archive,
- detailed approval workflow,
- WordPress credentials.

# Output

Create `project-context.md` from `project-context-template.md`.

Fill unknown details with short defaults. Use this wording where appropriate:

```text
Default: not specified during onboarding.
```

At the end, tell the user that `project-context.md` has been created and can be edited manually at any time.

# Rules

- Prefer short, decision-oriented questions.
- Reuse existing answers instead of re-asking them.
- Treat editorial review against existing content as optional, never default.
- In a fresh repository, `project-context.md` is expected to be missing. Create it through onboarding instead of inventing assumptions.
