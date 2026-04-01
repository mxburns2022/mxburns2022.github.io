# Content Templates

## Publication Template

Create a new file: `_publications/YYYY-MM-DD-title-slug.md`

```yaml
---
title: "Full Paper Title"
authors: "Your Name, Co-Author Name, Another Author"
venue: "Conference Name or Journal Name"
date: YYYY-MM-DD
paper: https://doi.org/xxxx or https://example.com/paper.pdf
code: https://github.com/username/repository
slides: https://example.com/slides.pdf
video: https://youtube.com/watch?v=xxxxx
poster: https://example.com/poster.pdf
tags: [tag1, tag2, tag3]
excerpt: "One sentence summary of the research contribution."
---

## Abstract

Longer description of the paper. Include main contributions, methodology, and key findings.

## Key Contributions

- Contribution 1
- Contribution 2
- Contribution 3

## Methods

Description of methods used...

## Results

Key results and findings...

## Conclusion

Brief conclusion...
```

---

## Blog Post Template

Create a new file: `_blog/YYYY-MM-DD-title-slug.md`

```yaml
---
title: "Blog Post Title"
date: YYYY-MM-DD
author: "Your Name"
category: research
tags: [tag1, tag2, tag3]
excerpt: "Brief excerpt that appears in blog listings and feeds."
---

## Introduction

Opening paragraph introducing the topic...

## Main Section 1

Discussion of topic...

```python
# Code examples can be included
def example_function(x):
    return x * 2
```

## Main Section 2

More discussion...

## Conclusion

Concluding thoughts...

## References

- [Reference 1](https://example.com)
- [Reference 2](https://example.com)
```

---

## Project Template

Create a new file: `_projects/project-name.md`

```yaml
---
title: "Project Name"
description: "One-line description of what the project does"
github: https://github.com/username/project-name
website: https://project-website.com
documentation: https://docs.example.com
language: Python
languages: [Python, C++, CUDA]
status: Active
featured: true
tags: [simulation, gpu, scientific-computing]
---

## Overview

Brief overview of the project and its purpose...

## Features

- Feature 1
- Feature 2
- Feature 3

## Installation

```bash
git clone https://github.com/username/project-name.git
cd project-name
pip install -e .
```

## Quick Start

```python
import project_name

# Example usage
result = project_name.compute(data)
print(result)
```

## Performance

Benchmarks, speed comparisons, or performance characteristics...

## Applications

- Use case 1
- Use case 2
- Use case 3

## Documentation

Full documentation available at [GitHub](https://github.com/username/project-name)

## Citation

If your project is published, include citation information:

```bibtex
@software{example2024,
  author = {Your Name},
  title = {Project Name},
  year = {2024},
  url = {https://github.com/username/project-name}
}
```

## License

Project license information...
```

---

## Publication Example (Filled)

```yaml
---
title: "Efficient Distributed Training of Neural Networks on Heterogeneous Clusters"
authors: "John Smith, Jane Doe, Robert Johnson"
venue: "Proceedings of the 35th International Conference on Machine Learning (ICML)"
date: 2024-07-15
paper: https://proceedings.mlr.press/v235/smith24a.html
code: https://github.com/example/distributed-training
slides: https://example.com/icml-slides.pdf
video: https://youtube.com/watch?v=dQw4w9WgXcQ
tags: [distributed-learning, optimization, deep-learning]
excerpt: "We propose a novel gradient compression scheme that enables efficient training of large neural networks on heterogeneous GPU clusters."
---

## Abstract

Training large neural networks across distributed computing environments remains challenging due to heterogeneous hardware and communication bottlenecks. We present a novel gradient compression algorithm...
```

---

## Frontmatter Field Reference

### Publication Fields
- `title` (required): Paper title
- `authors` (required): Comma-separated author list
- `venue` (required): Conference/journal name
- `date` (required): Publication date (YYYY-MM-DD)
- `excerpt` (required): One-sentence summary
- `paper`: URL to paper PDF
- `code`: GitHub repository link
- `slides`: Presentation slides
- `video`: YouTube or video link
- `poster`: Conference poster
- `tags`: YAML list of tags

### Blog Post Fields
- `title` (required): Post title
- `date` (required): Publication date (YYYY-MM-DD)
- `author`: Author name (defaults to site author)
- `category`: Category (e.g., "research", "tutorial")
- `tags`: YAML list of tags
- `excerpt` (required): Preview text

### Project Fields
- `title` (required): Project name
- `description` (required): One-line description
- `github`: GitHub repository URL
- `website`: Project website
- `documentation`: Documentation link
- `language`: Primary language
- `languages`: YAML list of languages used
- `status`: Current status (Active, Inactive, etc.)
- `featured`: Boolean for homepage featuring
- `tags`: YAML list of tags

---

## Tips for Writing Good Content

### Publications
- Keep excerpts to 1-2 sentences
- Use academic venue names (not just conference codes)
- Include DOI or link to published version
- Link code repositories for reproducibility
- Use tags that match your research areas

### Blog Posts
- Write for your target audience
- Use clear headings and structure
- Include code examples when relevant
- Add links to related publications
- Update the excerpt regularly
- Use consistent naming: `YYYY-MM-DD-slug`

### Projects
- Write clear READMEs
- Include installation instructions
- Provide usage examples
- Document dependencies
- List key features
- Include performance information
- Add citation information if published

---

## Quick Reference

### Add a publication:
```bash
touch _publications/YYYY-MM-DD-slug.md
# Edit file with template above
```

### Add a blog post:
```bash
touch _blog/YYYY-MM-DD-slug.md
# Edit file with template above
```

### Add a project:
```bash
touch _projects/project-slug.md
# Edit file with template above
```

### View locally:
```bash
bundle exec jekyll serve
# Visit http://localhost:4000
```

### Deploy to GitHub Pages:
```bash
git add .
git commit -m "Add new content"
git push origin main
```
