# Yi-Chun Hung — Academic Website

This is a custom Hugo site for GitHub Pages. Its four page-content files are deliberately separated from the shared HTML and CSS templates.

## Edit content

- `content/_index.md` — Home profile, biography, and news
- `content/research.md` — Research experience and current research areas
- `content/publications.md` — Journal, conference, preprint, and patent publications
- `content/experience.md` — Education, talks, academic service, and awards

The files use YAML front matter. Add or edit entries in the relevant list; the Hugo templates handle layout and ordering.

Publication labels are chronological within each type: the earliest conference and journal papers start at `C0` and `J0`. Give each item a stable BibTeX-style `id`; when adding a new paper, use the next available `C` or `J` number without renumbering earlier entries.

## Preview locally

```sh
hugo server
```

Then open `http://localhost:1313/`.

## Production build

```sh
hugo --minify
```

The generated site is written to `public/`, which is intentionally ignored by Git.

## Deploy

The included GitHub Actions workflow builds and publishes the site whenever changes reach `master`. In the repository settings, set **Pages → Build and deployment → Source** to **GitHub Actions** once before the first deployment.
