# Portfolio

Personal portfolio site for Angelo Pana, built with [Hugo](https://gohugo.io). No theme, no JavaScript, one stylesheet.

## Editing

- `config.toml`: name, headline and contact links
- `content/_index.md`: the About text
- `data/skills.yml`, `data/experience.yml`, `data/education.yml`
- `content/portfolio/*.md`: one file per project, with thumbnails in `assets/images/portfolio/`
- `assets/css/main.css`: all styling

Everything in `config.toml` ends up in the public HTML, so never put secrets there.

## Preview and publish

```sh
hugo server -O               # preview at http://localhost:1313 and open it in your browser
hugo --cleanDestinationDir   # build the site into docs/
```
