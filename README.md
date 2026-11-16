# Tarek Nasser — Personal site & blog

Built with [Hugo](https://gohugo.io/) using a custom, dependency-free theme (layouts in `layouts/`, styles in `static/css/main.css`).

## Local development

```bash
hugo server
# open http://localhost:1313
```

## Writing a post

Create a Markdown file under `content/posts/`:

```bash
hugo new posts/my-post.md
```

Front matter:

```yaml
---
title: "My Post Title"
date: 2025-01-01
tags: ["devops", "notes"]
---
```

Drafts (`draft: true`) are hidden in production. Posts with a future `date` are hidden until that date.

## Configuration

Site identity, bio, and social links live in `hugo.toml` under `[params]`.

Apps (home page and `/apps/`) are listed in `data/apps.yaml`, with icons in
`assets/img/apps/`. Skills, experience, certifications, and education (home
page and `/about/`) live in `data/resume.yaml`.
Recolor the whole site by changing `--accent` in `static/css/main.css`.

## Deployment

Pushing to `main` triggers `.github/workflows/hugo.yml`, which builds the site
and deploys it to GitHub Pages. Enable it once under **Settings → Pages →
Build and deployment → Source: GitHub Actions**.
