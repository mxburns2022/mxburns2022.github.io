---
layout: default
title: Publications
---

<div class="container">
    <h1>{{ page.title }}</h1>
    <p class="section-subtitle">Research publications and peer-reviewed work</p>

    {% if site.publications.size > 0 %}
        <div class="publications-list">
            {% assign sorted_pubs = site.publications | sort: 'date' | reverse %}
            {% for pub in sorted_pubs %}
                <article class="publication-card">
                    <h3><a href="{{ pub.url }}">{{ pub.title }}</a></h3>
                    {% if pub.authors %}
                        <p class="authors">{{ pub.authors }}</p>
                    {% endif %}
                    {% if pub.venue %}
                        <p class="venue"><em>{{ pub.venue }}</em> ({{ pub.date | date: "%Y" }})</p>
                    {% endif %}
                    {% if pub.excerpt %}
                        <p class="excerpt">{{ pub.excerpt }}</p>
                    {% endif %}
                    <div class="publication-links">
                        {% if pub.paper %}
                            <a href="{{ pub.paper }}" class="btn btn-small" target="_blank" rel="noopener">📄 Paper</a>
                        {% endif %}
                        {% if pub.code %}
                            <a href="{{ pub.code }}" class="btn btn-small" target="_blank" rel="noopener">💻 Code</a>
                        {% endif %}
                        {% if pub.slides %}
                            <a href="{{ pub.slides }}" class="btn btn-small" target="_blank" rel="noopener">📊 Slides</a>
                        {% endif %}
                        {% if pub.video %}
                            <a href="{{ pub.video }}" class="btn btn-small" target="_blank" rel="noopener">🎥 Video</a>
                        {% endif %}
                        {% if pub.poster %}
                            <a href="{{ pub.poster }}" class="btn btn-small" target="_blank" rel="noopener">🖼️ Poster</a>
                        {% endif %}
                    </div>
                </article>
            {% endfor %}
        </div>
    {% else %}
        <p class="placeholder">No publications yet. Check back soon!</p>
    {% endif %}
</div>
