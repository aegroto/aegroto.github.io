# aegroto-website

Personal academic website of **Lorenzo Catania** — Research Fellow in Computer Science @ University of Catania (DMI). 
Also known as **aegroto** around the internet.

Built with [Zola](https://www.getzola.org/) (v0.23.6). 

## Structure

- `config.toml` — site metadata, menu, profile links
- `content/_index.md` — homepage
- `content/publications/` — full publications list 
- `content/teaching/` — teaching activities
- `content/open-source/` — maintained projects + notable upstream contributions
- `templates/` — `base.html`, `index.html`, `section.html`
- `static/css/style.css` — theme (no JS, responsive)

## Develop

```bash
zola serve      # local preview at http://127.0.0.1:1111
zola build      # output in public/
zola check      # validate links (optional)
```
