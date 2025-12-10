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
    <p class="profile-bio">"In theory, theory and practice are the same. In practice, they are not" - Albert Einstein</p>
    
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
    <p>Welcome to my website, I am a Computer Science @ Georgia Tech. In the project section of the website, it will describe about the projects that I have been working on and completed</p>
  </div>
</div>

<div class="projects-container">
  <h2>Featured Projects</h2>
  
  {% assign project_posts = site.posts | where_exp: "post", "post.categories contains 'projects'" %}
  {% if project_posts.size > 0 %}
    <div class="projects-list">
      {% for post in project_posts limit: 3 %}
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
  
  {% if project_posts.size > 3 %}
    <div class="view-all">
      <a href="{{ '/projects/' | relative_url }}" class="view-all-link">View All Projects →</a>
    </div>
  {% endif %}
</div>
