---
layout: default
title: Projects
permalink: /projects/
---

<div class="projects-container">
  <h1>My Projects</h1>
  <p class="projects-intro">Collection of projects and work.</p>

  {% assign project_posts = site.posts | where_exp: "post", "post.categories contains 'projects'" %}
  {% if project_posts.size > 0 %}
    <div class="projects-list">
      {% for post in project_posts %}
        <article class="project-card">
          <h3 class="project-title">
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </h3>
          <p class="project-date">{{ post.date | date: "%B %d, %Y" }}</p>
          <p class="project-excerpt">{{ post.excerpt | strip_html | truncatewords: 40 }}</p>
          <a href="{{ post.url | relative_url }}" class="read-more">Read More →</a>
        </article>
      {% endfor %}
    </div>
  {% else %}
    <p class="no-posts">No projects yet. Check back soon!</p>
  {% endif %}
</div>
