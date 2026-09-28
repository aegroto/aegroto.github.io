# aegroto-website

Personal academic website of **Lorenzo Catania** — Research Fellow in Computer Science @ University of Catania (DMI).

Built with [Zola](https://www.getzola.org/) (v0.23.6). 

## Structure

- `config.toml` — site metadata, menu, profile links
- `content/_index.md` — homepage
- `content/publications/` — full list (from Google Scholar)
- `content/teaching/` — tutoring, seminars, ICIP 2024 tutorial
- `content/open-source/` — maintained projects (remotia, NIF) + notable upstream contributions
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
- Photos (`config.extra.avatar` / `config.extra.photo` in `config.toml`):
  - `static/images/avatar.png` — GitHub avatar (`https://avatars.githubusercontent.com/u/11978802?v=4`), shown in the top navbar. Re-download to refresh.
  - `static/images/photo.jpg` — homepage hero photo (1200px, q85 web export of `DSC_0271.JPG` from `foto etna`).
- Update publications from [Scholar](https://scholar.google.com/citations?user=bp4W1qoAAAAJ&hl=it).

## Deploy (GitHub Pages)

This repo is `aegroto.github.io` (user site) → served at <https://aegroto.github.io>.

- Push to `master`/`main`: the `Deploy Zola site to GitHub Pages` workflow builds with Zola 0.23.6 and deploys `public/` via `actions/deploy-pages`.
- One-time repo setup: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
- `base_url` in `config.toml` is already `https://aegroto.github.io`, matching the user-site URL.
