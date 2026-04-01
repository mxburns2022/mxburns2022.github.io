---
layout: default
title: Home
---

<section class="hero">
    <div class="hero-content">
        <div class="hero-text">
            <h1>{{ site.title }}</h1>
            <p class="subtitle">{{ site.description }}</p>
            <div class="hero-links">
                <a href="#about" class="btn btn-primary">About Me</a>
                <a href="/publications/" class="btn btn-secondary">Publications</a>
                <a href="/projects/" class="btn btn-secondary">Projects</a>
                <a href="/blog/" class="btn btn-secondary">Blog</a>
            </div>
        </div>
    </div>
</section>

<section id="about" class="about">
    <div class="container">
        <h2>About</h2>
        <div class="about-content">
            <p>
                Welcome to my research website. I'm passionate about advancing knowledge through rigorous research and 
                high-quality software engineering. Here you'll find my latest publications, research projects, and 
                insights on topics I care about.
            </p>
            <p>
                Feel free to explore my work across publications, code projects, and blog posts. You can also connect 
                with me on GitHub, Google Scholar, or LinkedIn.
            </p>
        </div>
    </div>
</section>

<section class="recent-publications">
    <div class="container">
        <h2>Recent Publications</h2>
        {% assign recent_pubs = site.publications | sort: 'date' | reverse | first: 3 %}
        
        {% if recent_pubs.size > 0 %}
            <div class="publications-list">
                {% for pub in recent_pubs %}
                    <article class="publication-card">
                        <h3><a href="{{ pub.url }}">{{ pub.title }}</a></h3>
                        {% if pub.authors %}
                            <p class="authors">{{ pub.authors }}</p>
                        {% endif %}
                        {% if pub.venue %}
                            <p class="venue"><em>{{ pub.venue }}</em> ({{ pub.date | date: "%Y" }})</p>
                        {% endif %}
                        <div class="publication-links">
                            {% if pub.paper %}
                                <a href="{{ pub.paper }}" target="_blank" rel="noopener">Paper</a>
                            {% endif %}
                            {% if pub.code %}
                                <a href="{{ pub.code }}" target="_blank" rel="noopener">Code</a>
                            {% endif %}
                        </div>
                    </article>
                {% endfor %}
            </div>
            <div class="view-all">
                <a href="/publications/" class="btn btn-secondary">View All Publications</a>
            </div>
        {% else %}
            <p class="placeholder">No publications yet. Check back soon!</p>
        {% endif %}
    </div>
</section>

<section class="recent-blog">
    <div class="container">
        <h2>Latest Blog Posts</h2>
        {% assign recent_posts = site.blog | sort: 'date' | reverse | first: 3 %}
        
        {% if recent_posts.size > 0 %}
            <div class="blog-list">
                {% for post in recent_posts %}
                    <article class="blog-card">
                        <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
                        <time datetime="{{ post.date | date_to_xmlschema }}" class="post-date">
                            {{ post.date | date: "%B %d, %Y" }}
                        </time>
                        <p>{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
                        <a href="{{ post.url }}" class="read-more">Read More →</a>
                    </article>
                {% endfor %}
            </div>
            <div class="view-all">
                <a href="/blog/" class="btn btn-secondary">View All Posts</a>
            </div>
        {% else %}
            <p class="placeholder">No blog posts yet. Check back soon!</p>
        {% endif %}
    </div>
</section>
