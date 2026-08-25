---
layout: default
title: Preprints
---

<div class="container listing-page">
    <p class="eyebrow">Work in progress</p>
    <h1>Preprints</h1>
    <p class="section-subtitle">Research papers that are currently available as preprints.</p>
    <div class="publications-list">
        {% assign sorted_preprints = site.preprints | sort: 'date' | reverse %}
        {% for preprint in sorted_preprints %}
        <article class="publication-card">
            <p class="item-kicker">Preprint · {{ preprint.date | date: "%Y" }}</p>
            <h2><a href="{{ preprint.url | relative_url }}">{{ preprint.title }}</a></h2>
            <p class="authors">{{ preprint.authors }}</p>
            {% if preprint.abstract %}<p class="excerpt">{{ preprint.abstract }}</p>{% endif %}
            {% if preprint.paper %}<a href="{{ preprint.paper }}" target="_blank" rel="noopener">Read on arXiv <span aria-hidden="true">↗</span></a>{% endif %}
        </article>
        {% endfor %}
    </div>
</div>
