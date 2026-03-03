# LIU Qianli's Academic Homepage

Personal academic homepage built with Jekyll (based on the Academic Pages theme).

- Site URL: `https://liu-km.github.io`
- Repository: `liu-km/liu-km.github.io`

## Project Structure

- `_config.yml`: site-level settings (name, bio, links, theme, etc.)
- `_pages/about.md`: homepage content (`/`)
- `_data/news.yml`: news list shown on homepage
- `_data/publications.yml`: publication list shown on homepage
- `_data/teaching.yml`: teaching experience
- `_data/awards.yml`: awards
- `_data/academic_service.yml`: academic service
- `_publications/`: publication detail pages (collection pages)
- `images/`: static images used by the site
- `files/`: downloadable files (papers, slides, CV, etc.)
- `assets/`: CSS/JS/fonts

## Daily Update Workflow

1. Update personal profile in `_config.yml` (`author`, `title`, `bio`, links).
2. Update homepage sections in `_data/*.yml`.
3. Add/modify detailed publication pages in `_publications/*.md` when needed.
4. If top navigation is needed, edit `_data/navigation.yml`.

## Run Locally

### Option 1: Native Ruby/Jekyll

```bash
bundle install
bundle exec jekyll serve -l -H localhost
```

Then open `http://localhost:4000`.

### Option 2: Docker

```bash
docker compose up
```

Then open `http://localhost:4000`.

## Deployment

This repo is intended for GitHub Pages deployment. Push to the default branch and wait for GitHub Actions Pages build to finish.

## Notes

- This repository has been cleaned up from most template demo/sample files.
- Some placeholder content may still exist in data/publication entries (for example `TITLE_PLACEHOLDER`) and should be replaced as you finalize content.
