# md-to-html

A single-file, browser-only Markdown → HTML converter with a slick UI. Drop a `.md` file, hit **Convert**, and an optimized standalone HTML pops up in a new tab.

No server, no upload, no build step — just open `index.html`.

## Features

- **Drag & drop** or browse for `.md` / `.markdown` / `.txt` files
- **Live editing** — tweak the markdown before converting
- **Optimized output:**
  - GitHub-flavored Markdown (tables, task lists, fenced code) via [marked](https://github.com/markedjs/marked)
  - Clean GitHub-style typography, max-width reading column
  - Auto light/dark via `prefers-color-scheme`
  - Syntax highlighting via [highlight.js](https://highlightjs.org/)
  - Optional auto-generated table of contents
  - Print-friendly styles
- **Two outputs:** open in new tab, or download the `.html`
- Everything runs client-side — nothing is uploaded

## Usage

### Online
[Open the live page](https://fourier18.github.io/md-to-html/) (once GitHub Pages is enabled on this repo).

### Locally
Clone or download, then open `index.html` in any modern browser.

```bash
git clone https://github.com/Fourier18/md-to-html.git
cd md-to-html
# Just open index.html — that's it.
```

## How it works

The page bundles a small UI that uses `marked` (loaded from jsDelivr) to parse the markdown, then assembles a fully self-contained HTML document — embedded styles, optional CDN links for highlight.js — and serves it via a Blob URL opened in a new tab.

The generated HTML has no dependency on this app and will render correctly anywhere it's opened.

## Credits

- **Author:** Claude (Anthropic, Opus 4.7) — wrote the code
- **Creative Director:** Joshua ([@Fourier18](https://github.com/Fourier18)) — set the brief, made the calls, signed off

Built in a single Claude Code session.

## License

MIT — see [LICENSE](LICENSE).
