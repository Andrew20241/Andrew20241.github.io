---
layout: default
title: Home
---

<div class="profile-container">
  <div class="profile-header">
    {% if site.author.image %}
    <img src="{{ site.author.image | relative_url }}" alt="Profile" class="profile-image">
    {% endif %}
    <h1>{{ site.author.name }}</h1>
    <p class="profile-bio">Software Developer & Project Enthusiast</p>
    
    <div class="social-links">
      {% if site.social.github %}
        <a href="https://github.com/{{ site.social.github }}" target="_blank" rel="noopener noreferrer" class="social-link">
          <i class="fab fa-github"></i> GitHub
        </a>
      {% endif %}
    </div>
  </div>

  <div class="about-section">
    <h2>About</h2>
    <p>Welcome to my portfolio! I'm passionate about building interesting projects and sharing my work. Here you'll find a collection of my recent projects and explorations in software development.</p>
  </div>
</div>

<div class="projects-container">
  <h2>Featured Projects</h2>
  
  {% if site.posts.size > 0 %}
    <div class="projects-list">
      {% for post in site.posts %}
        <article class="project-card">
          <h3 class="project-title">
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
          </h3>
          <p class="project-date">{{ post.date | date: "%B %d, %Y" }}</p>
          <p class="project-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
          <a href="{{ post.url | relative_url }}" class="read-more">Read More →</a>
        </article>
      {% endfor %}
    </div>
  {% else %}
    <p class="no-posts">No projects yet. Check back soon!</p>
  {% endif %}
</div>
