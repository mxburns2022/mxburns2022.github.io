# Research Website Setup Complete

Your research-focused Jekyll website has been successfully created with all essential components for showcasing publications, blog posts, and code projects.

## 📁 What's Been Created

### Core Structure
- **`_config.yml`**: Site configuration (title, author, social links, collections setup)
- **`Gemfile`**: Ruby dependencies for Jekyll
- **`.gitignore`**: Standard Jekyll/Ruby ignores

### Layouts & Components
- **`_layouts/default.html`**: Base page layout
- **`_layouts/post.html`**: Blog post template
- **`_layouts/publication.html`**: Publication template with links
- **`_layouts/project.html`**: Project showcase template
- **`_includes/header.html`**: Navigation bar
- **`_includes/footer.html`**: Footer with social links

### Pages
- **`index.md`**: Home page with hero section and recent items
- **`publications.md`**: Publications archive
- **`blog.md`**: Blog archive
- **`projects.md`**: Projects showcase

### Content Collections
- **`_publications/`**: Research publications (2 examples included)
- **`_blog/`**: Blog posts (2 examples included)
- **`_projects/`**: Code projects (2 examples included)

### Styling
- **`assets/css/style.css`**: Modern, responsive design with:
  - Clean typography and layout
  - Dark hero gradient section
  - Card-based content display
  - Mobile-responsive grid layouts
  - Smooth transitions and hover effects
  - Dark footer with social icons
  - Print-friendly styling

### Documentation
- **`README.md`**: Overview and directory structure
- **`QUICKSTART.md`**: Step-by-step setup and customization guide

## 🚀 Getting Started

### 1. Install Dependencies
```bash
cd /home/matt/Documents/development/personal/mxburns2022.github.io
bundle install
```

### 2. Run Development Server
```bash
bundle exec jekyll serve
```
Visit `http://localhost:4000`

### 3. Customize Configuration
Edit `_config.yml`:
```yaml
title: "Your Name"
author: "Your Name"
email: "your.email@example.com"
description: "Your research description"
github_username: your-github-id
google_scholar: "your-scholar-id"
linkedin_username: your-linkedin-id
```

### 4. Update Home Page
Edit `index.md` to customize the hero section and about text.

## 📝 Adding Content

### New Publication
Create `_publications/YYYY-MM-DD-title.md`:
```yaml
---
title: "Paper Title"
authors: "Your Name, Co-Author"
venue: "Journal/Conference Name"
date: 2024-01-15
paper: https://example.com/paper.pdf
code: https://github.com/example
tags: [machine-learning, parallel-computing]
excerpt: "Brief description..."
---

## Abstract
Publication content...
```

### New Blog Post
Create `_blog/YYYY-MM-DD-title.md`:
```yaml
---
title: "Post Title"
date: 2024-01-15
tags: [research, tutorial]
excerpt: "Brief excerpt..."
---

Blog content...
```

### New Project
Create `_projects/project-name.md`:
```yaml
---
title: "Project Name"
description: "What it does"
github: https://github.com/user/project
language: Python
status: Active
---

## Overview
Project details...
```

## 🎨 Customization

### Change Colors
Edit `assets/css/style.css` and modify the root variables:
```css
:root {
    --color-primary: #0066cc;
    --color-secondary: #f0f0f0;
    --color-text: #222;
    /* etc. */
}
```

### Modify Layout
- Edit `_layouts/default.html` for the overall structure
- Edit `_includes/header.html` for navigation
- Edit `_includes/footer.html` for footer content

### Add Images
Place images in `assets/images/` and reference them:
```markdown
![Alt text](/assets/images/filename.png)
```

## 🔗 Social Integration

The site automatically includes links to:
- **GitHub**: `github.com/{github_username}`
- **Google Scholar**: `scholar.google.com/citations?user={google_scholar_id}`
- **LinkedIn**: `linkedin.com/in/{linkedin_username}`

Configure these in `_config.yml`.

## 📊 Featured Content

### Homepage Display
- **Recent Publications**: Shows 3 latest publications
- **Recent Blog Posts**: Shows 3 latest blog posts
- Quick navigation to full archives

### Archive Pages
- **Publications Page**: Full list of all publications with filtering
- **Blog Page**: Complete blog archive
- **Projects Page**: Grid layout of code projects

## ✨ Key Features

✅ **Easy Content Management**: Add posts/pubs with simple YAML frontmatter
✅ **Google Scholar Integration**: Direct links to your scholar profile
✅ **GitHub Showcase**: Display and link to code projects
✅ **Responsive Design**: Beautiful on desktop, tablet, and mobile
✅ **Fast & Lightweight**: Static site generation - extremely fast
✅ **GitHub Pages Ready**: Deploy free to GitHub Pages
✅ **SEO Optimized**: Built-in meta tags and structured data
✅ **Clean Code**: Well-organized, commented CSS and HTML

## 🚢 Deployment

### GitHub Pages
1. Push to a GitHub repository named `username.github.io`
2. Enable GitHub Pages in settings
3. Your site will be live at `https://username.github.io`

### Custom Domain
1. Add a `CNAME` file with your domain name
2. Configure DNS records
3. Enable HTTPS in GitHub Pages settings

## 📚 Sample Content Included

### Publications
1. **Efficient Parallel Computing Techniques** (2024)
   - Example publication with paper, code, and links
   
2. **Machine Learning for Scientific Computing** (2024)
   - Example with slides and additional resources

### Blog Posts
1. **Getting Started with High-Performance Computing**
   - HPC concepts, tools, and best practices
   
2. **Best Practices for Research Code**
   - Software engineering principles for research

### Projects
1. **SimPy: Simulation Framework**
   - Python discrete-event simulation
   
2. **FastSolver: High-Performance Linear Algebra**
   - GPU-accelerated library example

## 🔧 Troubleshooting

**Issue**: Jekyll won't start
- Ensure Ruby 2.5+ is installed: `ruby --version`
- Run: `bundle install`
- Delete `_site/` and `.jekyll-cache/` folders

**Issue**: Changes not showing
- Restart Jekyll server (Ctrl+C, then `bundle exec jekyll serve`)
- Clear browser cache (Ctrl+Shift+Del)
- Check `_config.yml` changes require server restart

**Issue**: Styles not loading
- Check CSS path is correct in `_layouts/default.html`
- Verify `assets/css/style.css` exists
- Clear browser cache

## 📖 Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Guide](https://pages.github.com/)
- [Markdown Syntax](https://www.markdownguide.org/)
- [YAML Reference](https://yaml.org/spec/)

## 🎯 Next Steps

1. **Install Jekyll**: Follow QUICKSTART.md
2. **Customize _config.yml**: Update title, author, social links
3. **Add your photo**: Place in `assets/images/` and update `index.md`
4. **Add your publications**: Create files in `_publications/`
5. **Start blogging**: Create first post in `_blog/`
6. **Deploy**: Push to GitHub Pages

## 📧 Need Help?

- Check `QUICKSTART.md` for detailed setup instructions
- Review included sample files for formatting examples
- See Jekyll docs for advanced customization

---

**Your research website is ready to go!** 🎉
