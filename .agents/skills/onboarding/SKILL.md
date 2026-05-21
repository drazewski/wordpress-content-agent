---
name: onboarding
description: Quickly create project-context.md for an article workflow before article creation starts.
aliases:
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
- Ask exactly one question at a time. Wait for the user's answer before asking the next question.
- Prefer multiple-choice style suggestions and defaults.
- Remind the user that missing details can be added later by editing `project-context.md`.
- Do not ask for long lists, detailed style rules, examples, or phrases to avoid during first onboarding.
- If the user gives a vague answer, use a reasonable default and mark it as a default in `project-context.md`.
- Do not start article writing during onboarding.
- Do not publish anything.

# Required questions

Ask these questions one at a time. Do not group multiple questions in one message.

1. What is the site, publication, or project about?

2. Who is the main reader?

3. What kind of articles should the agent usually create?
   - suggested choices: guides, news, research summaries, analyses, reviews, opinion/commentary

4. What tone should the articles use?
   - suggested choices: factual, approachable, expert, conversational, formal

5. What length should articles usually have?
   - suggested choices: short, medium (default), long, depends on topic

6. Should articles use headings?
   - suggested choices: yes, use H2/H3 headings (default); no, avoid headings unless requested; only for longer articles

7. Should articles include links to cited sources?
   - suggested choices: yes (default), no, only when external research is used

8. Where will article material usually come from?
   - suggested choices: local files in `source/`, user-provided links, web research, mixed

9. Can the agent use external web research when local material is not enough?
   - suggested choices: yes, only after asking, no

10. Should finished articles also be exported to WordPress drafts after the local Markdown file is created?
   - suggested choices: no, Markdown file only (default); yes, Markdown file plus WordPress draft after approval

11. Do you already have fixed categories or tags?
   - suggested choices: no, yes and I will provide them later, yes and I will provide them now

12. What is your prefer language for creating articles?
   - suggested choices: English (default), other (please specify)

# Optional follow-up only if needed

Ask these only when the user's earlier answers make them necessary:

- Is there a specific CMS API/proxy setup already available?
- If WordPress draft export is selected: are credentials and API settings already available in `.env`?

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
- CMS credentials.

# Output

Create `project-context.md` from `project-context-template.md`.

Fill unknown details with short defaults. Use this wording where appropriate:

```text
Default: not specified during onboarding.
```

At the end, tell the user that `project-context.md` has been created and can be edited manually at any time.

Always record that Markdown export to `articles/` is the base output. WordPress draft creation, when selected, is an additional optional step and does not replace the Markdown file.

# Rules

- Prefer short, decision-oriented questions.
- Reuse existing answers instead of re-asking them.
- Treat editorial review against existing content as optional, never default.
- In a fresh repository, `project-context.md` is expected to be missing. Create it through onboarding instead of inventing assumptions.
