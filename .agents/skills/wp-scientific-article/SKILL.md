---
name: wp-scientific-article
description: Analyze scientific papers, reports, PDFs, and other source documents from /source to extract reliable facts for an article draft.
---

# Expected source files in /source

## Scientific and expert publications

- Topic folders may contain `pdf`, `doc`, `docx`, `html`, `txt`, or `md` files.
- These files may include research papers, reports, white papers, expert analyses, datasets, or working notes.
- If a file cannot be decoded or read, state that immediately instead of guessing.
- Abstracts, summaries, conclusions, tables, and methodology sections are usually the most valuable starting points.
- Pay attention to results the authors describe as important, new, unexpected, or especially relevant.
- Capture numbers, dates, study conditions, sample sizes, and limitations when available.

## Text files and instructions

Some folders may include `.txt` or `.md` files with:

- additional context,
- instructions for the article,
- raw notes,
- lists of URLs worth reviewing,
- topic boundaries or publishing goals.

## How to work

1. Identify what comes directly from the sources and what is only interpretation.
2. Extract the core findings in plain language.
3. Preserve source details that matter: authors, publication date, place, method, scale, limits.
4. Flag missing information instead of filling gaps with assumptions.
5. Prepare a reliable factual base for the article that can later be shaped by `wp-style`.

