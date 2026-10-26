# Lorenzo Niccoli | Personal Website

This repository contains the source code for my personal website.

## Live Site
The site is deployed at: [lorenzoniccoli.github.io](https://lorenzoniccoli.github.io)

## Technical Architecture
*   **Static Site Generator:** Jekyll
*   **Hosting:** GitHub Pages
*   **Content Management:** Markdown and Liquid templates

## Project Structure
*   `cv.md`: Professional background and experience.
*   `publications.md`: Template for the research papers and conferences.
*   `_data/publications.yml` and `_data/conferences.yml`: Research papers and conference presentations.
*   `photos.md`: Pictures I took while traveling.
*   `assets/main.scss`: Shared styles and responsive layouts.

## Updating publications and conferences
Edit the files in `_data` rather than the generated HTML. Add new entries at
the top to display them first; publication numbers are assigned automatically.
Author names matching `author` in `_config.yml` are highlighted.

For a new publication, copy an existing entry and update its `authors`, `title`,
`journal`, `volume`, `issue`, `pages`, `year`, and `doi`. `issue` may be omitted
when not applicable. For a conference, supply `date`, `name`, `location`, and
`type`; add `title` for a presentation with a title. Quote YAML values containing
special characters such as `: ` (a colon followed by a space).

## Local Development
Use the Ruby version specified in `.ruby-version` and the Bundler version listed
at the end of `Gemfile.lock`. To build and preview the site locally, execute the
following commands in the project root:

```bash
bundle install
bundle exec jekyll serve
```
The local server will be accessible at `http://localhost:4000`.

The checked-in `_site` directory is generated output. To refresh it for
production, run `JEKYLL_ENV=production bundle exec jekyll build`.
