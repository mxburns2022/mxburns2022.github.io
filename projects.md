---
layout: default
title: Projects
---

<div class="container">
    <h1>{{ page.title }}</h1>
    <p class="section-subtitle">Code projects and software tools</p>

    {% if site.projects.size > 0 %}
        <div class="projects-grid">
            {% for project in site.projects %}
                <article class="project-card">
                    <h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
                    {% if project.description %}
                        <p class="description">{{ project.description }}</p>
                    {% endif %}
                    {% if project.language %}
                        <span class="language-badge">{{ project.language }}</span>
                    {% endif %}
                    <div class="project-links">
                        {% if project.github %}
                            <a href="{{ project.github }}" class="btn btn-small" target="_blank" rel="noopener">💻 GitHub</a>
                        {% endif %}
                    </div>
                </article>
            {% endfor %}
        </div>
    {% else %}
        <p class="placeholder">Add a Markdown file in <code>_projects/</code> to feature a GitHub project. The required fields are documented in <code>CONTENT_TEMPLATES.md</code>.</p>
    {% endif %}
</div>
