# README

This is a Jekyll-based portfolio website for showcasing your projects and accomplishments.

## Getting Started

### Prerequisites

- Ruby (2.7 or higher)
- Bundler

### Installation

1. Install dependencies:
```bash
bundle install
```

2. Start the development server:
```bash
bundle exec jekyll serve
```

3. Open your browser and visit `http://localhost:4000`

## Project Structure

```
.
├── _layouts/          # HTML layouts for pages and posts
├── _posts/            # Your project posts (use format: YYYY-MM-DD-title.md)
├── assets/
│   ├── css/           # Stylesheets
│   └── images/        # Images (your profile picture is here)
├── _config.yml        # Site configuration
├── index.md           # Homepage
└── Gemfile            # Ruby dependencies
```

## Writing a Project Post

1. Create a new file in `_posts/` directory with the format: `YYYY-MM-DD-title.md`
2. Add the front matter:

```markdown
---
layout: post
title: "Your Project Title"
date: YYYY-MM-DD
categories: projects
excerpt: "Brief description of your project"
---

Your project content in Markdown...
```

3. Your post will automatically appear on the homepage!

## Customization

Edit `_config.yml` to:
- Change your name and description
- Update your GitHub username
- Modify the site title and base URL

Edit `assets/css/style.css` to customize the appearance.

## Deployment

This site is ready to deploy to GitHub Pages:

1. Update `_config.yml` with your GitHub username (for the URL)
2. Push your changes to GitHub
3. Enable GitHub Pages in your repository settings

## Features

- ✅ Clean, minimal design
- ✅ Responsive mobile layout
- ✅ GitHub social link
- ✅ Project showcase
- ✅ Easy to customize

## Support

For more information about Jekyll, visit: https://jekyllrb.com
