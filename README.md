# tobiasmoenninger.com

Personal portfolio site for Tobias Moenninger, VFX Supervisor.
Built with Jekyll, hosted on GitHub Pages.

## Quick start

### 1. Create a GitHub repo

Create a new public repo named `tobiasmoenninger.github.io` (replace with
your GitHub username). Push this folder's contents to it.

### 2. Enable GitHub Pages

In the repo settings → Pages → Source: `Deploy from a branch` → Branch: `main` → `/` (root).

Your site will be live at `https://<your-username>.github.io` within a minute or two.

### 3. Custom domain

To keep `tobiasmoenninger.com`:

1. Create a file called `CNAME` in the repo root containing just `tobiasmoenninger.com`
2. In your domain registrar's DNS settings, add:
   - Four `A` records pointing `@` to: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - One `CNAME` record pointing `www` to `<your-username>.github.io`
3. In repo Settings → Pages → add custom domain → `tobiasmoenninger.com` and enable HTTPS

### 4. Contact form

1. Sign up at [formspree.io](https://formspree.io) (free tier)
2. Create a new form, copy the form ID (looks like `xyzabcde`)
3. Paste it into `_config.yml` under `formspree_id`

## Running locally

Requires Ruby 3.x.

```bash
bundle install
bundle exec jekyll serve
```

Visit `http://localhost:4000`.

## Content

### Adding a project

Create a new file in `_projects/`:

```markdown
---
title: My Film
category: Supervision   # or Compositing, Commercial, Cinematography
role: VFX Supervisor
company: Studio Name
year: 2025
thumbnail: /assets/images/my-film.jpg
hero_image: /assets/images/my-film-hero.jpg   # optional, large header image
vimeo_id: 123456789                           # optional
# youtube_id: dQw4w9WgXcQ                     # or this instead
---

Long-form description of the project in Markdown.
```

Thumbnails look best at 16:10 aspect ratio, ~1200x750px. Hero images around 2400x1200px.

### Adding a blog post

Create a file in `_posts/` named `YYYY-MM-DD-title.md`:

```markdown
---
title: "My post title"
date: 2026-05-01
excerpt: "Optional short summary shown in the blog list."
---

Your post, in Markdown.
```

### Editing About, Contact, etc.

Edit `about.md`, `contact.md`, `index.html` directly.

## Structure

```
.
├── _config.yml         # site settings
├── _layouts/           # page templates
├── _includes/          # shared partials (header, footer)
├── _projects/          # portfolio entries
├── _posts/             # blog posts
├── assets/
│   ├── css/style.scss
│   ├── js/main.js
│   └── images/         # put your project thumbnails here
├── index.html
├── about.md
├── portfolio.html
├── blog.html
└── contact.md
```
