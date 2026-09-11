# Portfolio

Angelo Pana's portfolio, built with [Hugo](https://gohugo.io) and the [Hugoplate](https://github.com/zeon-studio/hugoplate) theme (Tailwind CSS). The theme lives in `themes/hugoplate/` under its MIT license.

## Requirements

- Hugo **extended**, 0.158 to 0.166 (`brew install hugo`)
- Go (Hugo downloads the theme's add-on modules with it)
- Node.js and npm (Tailwind CSS)

## Run it

```sh
npm install        # once, and after pulling dependency changes
npm run dev        # preview at http://localhost:1313 (opens your browser, live reloads)
npm run build      # build the site into docs/
```

## Where things are

- `content/english/_index.md`: home page banner and the three feature blocks
- `content/english/about/_index.md`: About page
- `content/english/projects/`: one Markdown file per project (images in `assets/images/portfolio/`)
- `content/english/authors/angelo-pana.md`: author card shown on projects
- `content/english/sections/call-to-action.md` and `testimonial.md` (testimonials are off until there are real ones)
- `config/_default/params.toml`: header text, GitHub button, search, SEO description; everything here is public
- `config/_default/menus.en.toml`: header and footer menus
- `data/social.json`: footer social links
- `data/theme.json`: colors and fonts
- `layouts/`: the few overrides of Hugoplate templates (About page portrait size, PWA turned off)

## Security notes

- `static/_headers` sets security headers on Netlify or Cloudflare Pages. GitHub Pages ignores it.
- The PWA service worker is turned off (`layouts/_partials/pwa.html`), so visitors never get a stale cached copy.
- Raw HTML in Markdown is stripped (`hugo.toml`, `markup.goldmark.renderer.unsafe = false`).
