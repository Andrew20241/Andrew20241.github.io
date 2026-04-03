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
</div>
