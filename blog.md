---
layout: default
title: Blog
---

<div class="container">
    <h1>{{ page.title }}</h1>
    <p class="section-subtitle">Research insights and technical discussions</p>

    {% if site.blog.size > 0 %}
        <div class="blog-list">
            {% assign sorted_posts = site.blog | sort: 'date' | reverse %}
            {% for post in sorted_posts %}
                <article class="blog-card">
                    <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
                    <div class="post-meta">
                        <time datetime="{{ post.date | date_to_xmlschema }}" class="post-date">
                            {{ post.date | date: "%B %d, %Y" }}
                        </time>
                        {% if post.author %}
                            <span class="post-author">by {{ post.author }}</span>
                        {% endif %}
                    </div>
                    <p class="excerpt">{{ post.excerpt | strip_html }}</p>
                    <a href="{{ post.url }}" class="read-more">Read More →</a>
                </article>
            {% endfor %}
        </div>
    {% else %}
        <p class="placeholder">No blog posts yet. Check back soon!</p>
    {% endif %}
</div>
