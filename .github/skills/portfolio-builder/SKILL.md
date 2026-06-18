---
name: portfolio-builder
description: "Automatically populates, formats, and personalizes the anujsubra.github.io portfolio website using raw bio data. Use when updating the site, adding a new project, personalizing the style, or filling in bio details."
compatibility:
  - HTML/CSS
  - Jekyll
  - Astro
---

# Portfolio Builder Workflow

This skill guides workspace edits for Anuj Subra's portfolio site, focusing on Jekyll-based content and style updates.

## When to Use
- Updating the portfolio homepage or project sections
- Adding or editing project entries, publications, or talks
- Personalizing design, layout, or branding for the site
- Populating sections from raw bio data in `_data/portfolio-data.yml` or other content directories

## Step 1: Read Source Content
- Inspect raw data in `_data/portfolio-data.yml` first, then other source folders like `_portfolio/`, `_talks/`, `_posts/`, and `_publications/`.
- Identify key personal branding elements: technical experience, project outcomes, profile links, and professional themes.

## Step 2: Enforce Style & Personalization
- Apply a modern, minimalist, readable theme.
- Prefer clean monochrome or professional dark/light mode accents.
- Keep tone technical yet approachable; avoid generic marketing cliches.
- Use explicit `anujsubra` handles for GitHub/LinkedIn/other external links.

## Step 3: Execute Code Changes
- Update layouts, includes, or page content where the portfolio or bio is rendered.
- Organize images and assets under `assets/images/` or an equivalent site asset path.
- Ensure any new image references use relative URLs compatible with GitHub Pages.

## Step 4: Verify and Build
- Run the local build/serve command for the project.
- Typical commands: `bundle exec jekyll serve`, `npm run dev`, or another configured build task.
- Confirm no broken image paths, missing metadata, or local build failures.

## Step 5: Present and Commit
- Summarize visible changes and how the portfolio was updated.
- If approved, stage files and use a Conventional Commit message such as:
  - `feat(bio): add experience section`
  - `fix(portfolio): correct project link`
  - `style(site): improve portfolio layout`
