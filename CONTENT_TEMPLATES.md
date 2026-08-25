# Adding content

Each item is a Markdown file with a short YAML header. The filename determines its URL, so use a stable, descriptive name such as `2026-paper-title.md`.

## Publication

Create `_publications/YYYY-short-title.md`:

```yaml
---
title: "Paper title"
authors: "First Author, Matthew X. Burns, Coauthor"
venue: "Journal or conference"
date: 2026-01-01
paper: "https://doi.org/..."
code: "https://github.com/mxburns2022/repository" # optional
excerpt: "One-sentence summary for the listing page."
tags: [optimization, quantum-computing]
---

Optional abstract or notes.
```

## Preprint

Create `_preprints/YYYY-short-title.md`:

```yaml
---
title: "Preprint title"
authors: "Matthew X. Burns, Coauthor"
date: 2026-01-01
paper: "https://arxiv.org/abs/..."
abstract: "One-sentence summary for the listing page."
tags: [optimization]
---

Optional abstract or notes.
```

## GitHub project

Create `_projects/project-name.md`:

```yaml
---
title: "Project name"
description: "One-sentence description of the software."
github: "https://github.com/mxburns2022/repository"
language: Python
status: Active
tags: [research-software]
---

Project details, installation instructions, and examples.
```

Then run `bundle exec jekyll serve` and visit `http://localhost:4000` to preview changes.
