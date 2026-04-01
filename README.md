# Research Website

A Jekyll-based research website for showcasing publications, blog posts, and code projects.

## Setup

1. Install dependencies:
   ```bash
   bundle install
   ```

2. Run the development server:
   ```bash
   bundle exec jekyll serve
   ```

3. Visit `http://localhost:4000`

## Adding Content

### Publications
Create a new file in `_publications/` with YAML frontmatter:
```yaml
---
title: "Paper Title"
authors: "Your Name, Co-Author"
venue: "Conference/Journal Name"
date: 2024-01-15
paper: https://example.com/paper.pdf
code: https://github.com/example
google_scholar: true
---

Brief description of the publication...
```

### Blog Posts
Create a new file in `_blog/` with YAML frontmatter:
```yaml
---
title: "Blog Post Title"
date: 2024-01-15
category: research
---

Blog post content...
```

### Projects
Create a new file in `_projects/` with YAML frontmatter:
```yaml
---
title: "Project Name"
description: "Brief description"
github: https://github.com/example/project
language: Python
---

Project details...
```

## Directory Structure

```
.
├── _blog/              # Blog posts
├── _publications/      # Research publications
├── _projects/          # Code projects
├── _layouts/           # Page layouts
├── _includes/          # Reusable components
├── assets/             # CSS, images, fonts
├── index.md            # Home page
└── _config.yml         # Site configuration
```

## Customization

Edit `_config.yml` to update:
- Site title and description
- Social media links
- Google Scholar ID
- GitHub username
