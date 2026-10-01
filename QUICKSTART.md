# Quick Start Guide

## Installation & Setup

### 1. Install Ruby and Jekyll

On Ubuntu/Debian:
```bash
sudo apt-get update
sudo apt-get install ruby-full build-essential zlib1g-dev
echo '# Install Ruby Gems to ~/.gems' >> ~/.bashrc_custom
echo 'export GEM_HOME="$HOME/.gems"' >> ~/.bashrc_custom
echo 'export PATH="$HOME/.gems/bin:$PATH"' >> ~/.bashrc_custom
source ~/.bashrc
gem install jekyll bundler
```

On macOS (with Homebrew):
```bash
brew install ruby
echo 'export PATH="/usr/local/opt/ruby/bin:$PATH"' >> ~/.zshrc_custom
source ~/.zshrc
gem install jekyll bundler
```

### 2. Install Dependencies

In your project directory:
```bash
bundle install
```

## Running Locally

Start the development server:
```bash
bundle exec jekyll serve
```

Visit `http://localhost:4000` in your browser.

## File Structure Explained

```
.
├── _config.yml          # Main configuration file
├── _layouts/            # Page templates
│   ├── default.html     # Base layout
│   ├── post.html        # Blog post layout
│   ├── publication.html # Publication layout
│   └── project.html     # Project layout
├── _includes/           # Reusable components
│   ├── header.html      # Site header & navigation
│   └── footer.html      # Site footer with social links
├── _publications/       # Research publications
├── _blog/               # Blog posts
├── _projects/           # Code projects
├── assets/css/          # Stylesheets
├── index.md             # Home page
├── publications.md      # Publications archive
├── projects.md          # Projects archive
├── blog.md              # Blog archive
└── README.md            # This file
```

## Adding Content

### New Publication

Create `_publications/YYYY-MM-DD-title.md`:
```yaml
---
title: "Paper Title"
authors: "Your Name, Co-Author"
venue: "Conference/Journal Name"
date: 2024-01-15
paper: https://example.com/paper.pdf
code: https://github.com/example
slides: https://example.com/slides.pdf
tags: [tag1, tag2]
excerpt: "Brief description of the work..."
---

## Abstract

Your publication abstract and content...
```

### New Blog Post

Create `_blog/YYYY-MM-DD-title.md`:
```yaml
---
title: "Blog Post Title"
date: 2024-01-15
tags: [research, tutorial]
excerpt: "Brief excerpt..."
---

Your blog post content...
```

### New Project

Create `_projects/title.md`:
```yaml
---
title: "Project Name"
description: "Brief description of what the project does"
github: https://github.com/username/project
language: Python
status: Active
---

## Overview

Project details and README content...
```

## Customizing the Site

### Update Site Configuration

Edit `_config.yml`:
```yaml
title: "Your Name"
author: "Your Name"
email: "your.email@example.com"
github_username: your-github-username
google_scholar: "your-google-scholar-id"
linkedin_username: your-linkedin-id
```

### Customize Styling

Edit `assets/css/style.css` to change:
- Colors (root CSS variables)
- Typography
- Layout and spacing
- Responsive breakpoints

### Modify the Home Page

Edit `index.md` to customize the hero section and homepage layout.

## Deploying to GitHub Pages

### 1. Ensure Repository Settings

- Repository name should be `username.github.io`
- Set GitHub Pages source to "Deploy from a branch" (main/master)

### 2. Push to GitHub

```bash
git add .
git commit -m "Initial commit: research website"
git branch -M main
git remote add origin https://github.com/username/username.github.io.git
git push -u origin main
```

### 3. Access Your Site

Your site will be available at `https://username.github.io`

## Advanced Features

### Google Scholar Integration

The site includes built-in Google Scholar links. Update your Scholar ID in `_config.yml`:
```yaml
google_scholar: "your-id-here"
```

### GitHub Integration

Projects can link directly to GitHub repositories. Update project frontmatter:
```yaml
github: https://github.com/username/project-name
```

### Social Media Links

Add links to your social profiles in `_config.yml`:
- GitHub
- Google Scholar
- LinkedIn

These appear in the footer on every page.

## Tips & Best Practices

1. **Use meaningful URLs**: Jekyll automatically generates nice URLs from file names
2. **Write good frontmatter**: All front matter fields are searchable and filterable
3. **Keep posts organized**: Use consistent naming conventions (YYYY-MM-DD-slug)
4. **Link between content**: Reference related publications and blog posts
5. **Use tags**: Organize content with meaningful tags for easy navigation
6. **Write good excerpts**: The excerpt appears in archives and feeds
7. **Keep images in assets**: Store images in `assets/images/` for easy reference

## Troubleshooting

### Jekyll won't start
- Ensure Ruby and bundler are installed
- Run `bundle install` again
- Delete `_site/` and `.jekyll-cache/` folders, then try again

### Changes not appearing
- Changes to `_config.yml` require a server restart
- Clear your browser cache (Ctrl+Shift+Del)
- Check console for build errors

### Site looks broken locally
- Ensure you're using the correct base URL in development
- Check that all includes and layouts exist
- Verify CSS path in `_layouts/default.html`

## Further Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://pages.github.com/)
- [Markdown Guide](https://www.markdownguide.org/)
- [YAML Spec](https://yaml.org/)

## Support

For issues with Jekyll itself, visit the [Jekyll documentation](https://jekyllrb.com/).
For GitHub Pages issues, see [GitHub Help](https://docs.github.com/en/pages).
