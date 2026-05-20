---
name: wordpress-publish
description: Create or update WordPress draft posts from prepared article files using generic, reusable API rules.
---

# Requirements

- The target WordPress site or local proxy should be reachable.
- Credentials should be provided through `.env`, based on `.env.example`.
- Drafts should always stay in `draft` status unless the user explicitly chooses another workflow outside this template.
- Respect the publication mode defined during `onboarding`. If the project is Markdown-only, do not publish.

## Common endpoints

### Create draft

```text
POST {WP_API_BASE_URL}/posts
Content-Type: application/json
```

### Update existing draft

```text
POST {WP_API_BASE_URL}/posts/{id}
Content-Type: application/json
```

### Suggested body

```json
{
  "title": "Article title",
  "content": "<p>Article HTML</p>",
  "excerpt": "Short excerpt",
  "tags": [12, 15],
  "categories": [3],
  "status": "draft"
}
```

## Workflow

1. Read the finished article file from `articles/`.
2. Convert Markdown to WordPress-friendly HTML if needed.
3. Match category and tags to existing WordPress terms.
4. Create a new draft or update an existing one.
5. Confirm the returned post ID, title, link, and status.

## Rules

- Do not publish directly from this workflow.
- Update an existing post instead of creating duplicates when the draft already exists.
- Send tag and category IDs, not names.
- If the request fails, return the error clearly instead of masking it.
