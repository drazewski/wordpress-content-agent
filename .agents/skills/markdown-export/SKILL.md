---
name: markdown-export
description: Export a finished article draft to Markdown or MDX files with useful front matter.
---

# Purpose

Use this skill as the required base output adapter for finished article drafts.

This skill writes files only. It does not publish to a CMS and does not call external APIs. Publishing integrations may run later, but they do not replace this Markdown output.

# Default Output

Write finished drafts to:

```text
articles/<topic>.md
```

Use `.mdx` only when the user explicitly asks for MDX or when `project-context.md` requires it.

# Front Matter

Use YAML front matter when useful for the target workflow:

```yaml
---
title: ""
excerpt: ""
slug: ""
tags: []
category: ""
metaDescription: ""
---
```

# Body

After front matter, write the article in Markdown:

- use one `#` heading only if the target workflow expects it,
- use `##` and `###` headings for article sections,
- keep paragraphs readable,
- use lists only when they genuinely help,
- preserve source-backed facts, limitations, dates, and numbers.

# Sources

If sources are required by `project-context.md`, or if external research was used, include a final section:

```markdown
## Sources

- Source title, author or publisher, URL or file name.
```

# Rules

- Do not publish anywhere.
- Do not overwrite an unrelated article file.
- If `articles/<topic>.md` already exists, update it only when the user requested an update or the workflow clearly targets that topic.
- Keep front matter values consistent with the article, SEO, and taxonomy decisions.
- If a value is unknown, leave it empty or use a short explicit default rather than inventing details.
