---
layout: default
title: Home
---

<section class="hero hero--home">
  <div class="hero-content">
    <p class="eyebrow">Research portfolio</p>
    <h1>{{ site.title }}</h1>
    <p class="subtitle">{{ site.description }}</p>
    <div class="hero-links">
      <a href="{{ '/publications/' | relative_url }}" class="btn btn-primary">Publications</a>
      <a href="{{ '/preprints/' | relative_url }}" class="btn btn-secondary">Preprints</a>
      <a href="https://scholar.google.com/citations?user={{ site.google_scholar }}" class="btn btn-secondary" target="_blank" rel="noopener">Google Scholar</a>
      <a href="https://drive.google.com/file/d/1k2dCni705xGUS9vHd-PoC1pv5a03iebo/view?usp=sharing" class="btn btn-secondary" target="_blank" rel="noopener">CV</a>
    </div>
  </div>
</section>

<section class="about">
  <div class="container">
    <p class="eyebrow">About</p>
    <p class="intro">My work spans optimization, unconventional computing architectures, and high-performance computing. This site collects my publications, work in progress, and open-source research software.</p>
    <p>For the complete and current publication record, visit my <a href="https://scholar.google.com/citations?user={{ site.google_scholar }}" target="_blank" rel="noopener">Google Scholar profile</a>.</p>
  </div>
</section>

<section class="recent-preprints">
  <div class="container">
    <div class="section-heading"><div><p class="eyebrow">Work in progress</p><h2>Preprints</h2></div><a href="{{ '/preprints/' | relative_url }}">View all <span aria-hidden="true">→</span></a></div>
    {% assign recent_preprints = site.preprints | sort: 'date' | reverse %}
    <div class="publications-list">
      {% for preprint in recent_preprints limit: 2 %}
      <article class="publication-card">
        <p class="item-kicker">Preprint · {{ preprint.date | date: "%Y" }}</p>
        <h3><a href="{{ preprint.url | relative_url }}">{{ preprint.title }}</a></h3>
        <p class="authors">{{ preprint.authors }}</p>
        {% if preprint.abstract %}<p class="excerpt">{{ preprint.abstract }}</p>{% endif %}
      </article>
      {% endfor %}
    </div>
  </div>
</section>

<section class="recent-publications">
  <div class="container">
    <div class="section-heading"><div><p class="eyebrow">Selected work</p><h2>Publications</h2></div><a href="{{ '/publications/' | relative_url }}">View all <span aria-hidden="true">→</span></a></div>
    {% assign recent_pubs = site.publications | sort: 'date' | reverse %}
    <div class="publications-list">
      {% for pub in recent_pubs limit: 3 %}
      <article class="publication-card">
        <p class="item-kicker">{{ pub.date | date: "%Y" }}</p>
        <h3><a href="{{ pub.url | relative_url }}">{{ pub.title }}</a></h3>
        <p class="authors">{{ pub.authors }}</p>
        <p class="venue"><em>{{ pub.venue }}</em></p>
        {% if pub.excerpt %}<p class="excerpt">{{ pub.excerpt }}</p>{% endif %}
      </article>
      {% endfor %}
    </div>
  </div>
</section>

<section class="recent-projects">
  <div class="container">
    <div class="section-heading"><div><p class="eyebrow">Open source</p><h2>Projects</h2></div><a href="{{ '/projects/' | relative_url }}">View all <span aria-hidden="true">→</span></a></div>
    {% assign recent_projects = site.projects | sort: 'title' %}
    {% if recent_projects.size > 0 %}
    <div class="projects-grid">
      {% for project in recent_projects limit: 3 %}
      <article class="project-card"><h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3><p class="description">{{ project.description }}</p>{% if project.github %}<a href="{{ project.github }}" target="_blank" rel="noopener">GitHub <span aria-hidden="true">↗</span></a>{% endif %}</article>
      {% endfor %}
    </div>
    {% else %}
    <p class="placeholder">GitHub projects will appear here as they are added.</p>
    {% endif %}
  </div>
</section>
