# aegroto-website

Personal academic website of **Lorenzo Catania** — Research Fellow in Computer Science @ University of Catania (DMI).

Built with [Zola](https://www.getzola.org/) (v0.23.6). Inspired by [catalano.dmi.unict.it](https://catalano.dmi.unict.it/): sidebar with profile + menu, clean content pages.

## Structure

- `config.toml` — site metadata, menu, profile links
- `content/_index.md` — homepage
- `content/publications/` — full list (from Google Scholar)
- `content/teaching/` — tutoring, seminars, ICIP 2024 tutorial
- `content/projects/` — selected GitHub repos
- `content/contacts/` — email, address, profiles
- `templates/` — `base.html`, `index.html`, `section.html`
- `static/css/style.css` — theme (no JS, responsive)

## Develop

```bash
zola serve      # local preview at http://127.0.0.1:1111
zola build      # output in public/
zola check      # validate links (optional)
```

## Customize

- `base_url` in `config.toml` for deployment (GitHub Pages / custom domain).
- Add a photo: place `static/images/photo.jpg` (square, >=512px) and wire it in `templates/base.html` (see comment).
- Update publications from [Scholar](https://scholar.google.com/citations?user=bp4W1qoAAAAJ&hl=it).

## Deploy (GitHub Pages)

Any static host works. For GitHub Pages: build and push `public/` to `gh-pages`, or use a Zola GitHub Action.
