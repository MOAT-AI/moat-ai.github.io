# Repository Guidelines

## Project Structure & Module Organization

This repository is a Jekyll-based GitHub Pages site for the MOAT Collaboration homepage.

- `index.md`: homepage front matter and entry point
- `_layouts/home.html`: page layout that assembles the landing page
- `_sections/*.md`: markdown-backed homepage sections, ordered by filename/front matter
- `assets/css/site.css`: site styling
- `_config.yml`: Jekyll configuration
- `README.md`: brief project overview

There are no application modules or test directories yet; content is primarily markdown, HTML, CSS, and Jekyll config.

## Build, Test, and Development Commands

Only build/test locally when the user asks you, too.

- `bundle install`: install Ruby gems from `Gemfile`
- `bundle exec jekyll serve`: run the site locally with live reload
- `bundle exec jekyll build`: generate the static site into `_site/`

Local build artifacts are ignored by [`.gitignore`](/home/axel/src/moat-ai.github.io/.gitignore). Do not commit `_site/` or Jekyll cache files.

## Coding Style & Naming Conventions

Use short, readable markdown and keep placeholder text clearly labeled. Prefer ASCII unless a file already uses other characters.

- Markdown files: use clear headings and short sections
- HTML/CSS: use 2-space indentation
- Section files: keep numeric prefixes such as `_sections/01-introduction.md`
- Front matter keys: use lowercase snake_case where practical, for example `image_hint`

Keep styles centralized in `assets/css/site.css`; avoid inline styles unless there is a strong reason.

## Testing Guidelines

There is no automated test suite yet. For now, validate changes by:

- running `bundle exec jekyll serve` locally when possible
- checking that navigation anchors, section ordering, and markdown rendering work
- verifying responsive layout behavior on narrow and wide screens

If tests are added later, place them in a dedicated top-level directory and document the command here.

## Commit & Pull Request Guidelines

This repository has no commit history yet, so no established convention exists. Use short, imperative commit subjects such as `Add MOAT participants section` or `Refine homepage hero layout`.

Pull requests should include:

- a brief summary of the change
- linked issue or context when applicable
- screenshots for visible homepage/UI changes
- notes about any placeholder content or missing assets
