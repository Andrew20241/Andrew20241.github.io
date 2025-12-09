---
layout: default
title: Blog
permalink: /blog/
---

<div class="blog-container">
  <h1>Blog</h1>
  <p class="blog-intro">Thoughts, tutorials, and insights on software development and projects.</p>

  {% if site.posts.size > 0 %}
    <div class="blog-list">
      {% for post in site.posts %}
        <article class="blog-post-item">
          <div class="blog-post-header">
            <h2 class="blog-post-title">
              <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
            </h2>
            <p class="blog-post-date">
              <time datetime="{{ post.date | date_to_xmlschema }}">
                {{ post.date | date: "%B %d, %Y" }}
              </time>
            </p>
          </div>
          <p class="blog-post-excerpt">{{ post.excerpt | strip_html | truncatewords: 50 }}</p>
          <a href="{{ post.url | relative_url }}" class="read-more">Continue Reading →</a>
        </article>
      {% endfor %}
    </div>
  {% else %}
    <p class="no-posts">No blog posts yet. Check back soon!</p>
  {% endif %}
</div>
