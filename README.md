# Portfolio

Angelo Pana's single-page portfolio, built with [Hugo](https://gohugo.io) and the [Hugoplate](https://github.com/zeon-studio/hugoplate) theme (Tailwind CSS). The theme lives in `themes/hugoplate/` under its MIT license.

## Requirements

- Hugo **extended**, 0.158 to 0.166 (`brew install hugo`)
- Go (Hugo downloads the theme's add-on modules with it)
- Node.js and npm (Tailwind CSS)

## Run it

```sh
npm install        # once, and after pulling dependency changes
npm run dev        # preview at http://localhost:1313 (opens your browser, live reloads)
npm run build      # build the published site into docs/
```

Previews write to the gitignored `public/` folder; only `npm run build` writes to `docs/` (see `config/production/hugo.toml`).

## Where things are

Everything is on one page (`layouts/home.html`), in this order:

- Banner and the Skills, Experience and Education blocks: `content/english/_index.md` (each block's `id` is the anchor its menu link jumps to)
- About: `content/english/about/_index.md` (text and portrait)
- Projects: `content/english/projects/`, one Markdown file per project, shown in full (images in `assets/images/portfolio/`)
- Contact: `content/english/sections/call-to-action.md` (`testimonial.md` is off until there are real testimonials)

Settings:

- `config/_default/params.toml`: header text, GitHub button, SEO description and the security policy; everything here is public
- `config/_default/menus.en.toml`: header and footer links (`#section` anchors)
- `data/social.json`: footer social links
- `data/theme.json`: colors and fonts
- `layouts/_partials/`: small overrides of Hugoplate (style loading, PWA turned off)

## Security notes

- Every page gets a Content-Security-Policy and referrer policy from `custom_script` in `params.toml`. `static/_headers` adds more headers on Netlify or Cloudflare Pages; GitHub Pages ignores it.
- The PWA service worker is turned off (`layouts/_partials/pwa.html`), so visitors never get a stale cached copy.
- Raw HTML in Markdown is stripped (`hugo.toml`, `markup.goldmark.renderer.unsafe = false`).
