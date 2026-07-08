# thantzinmin.tech

Personal portfolio site, deployed via GitHub Pages.

## Structure

```
index.html       — the site (single page, deployed as-is; GitHub Pages requires it at root)
CNAME            — custom domain (thantzinmin.tech)
assets/js/       — support.js, the client-side runtime that renders index.html
assets/images/   — project screenshots/diagrams referenced from index.html
```

## Editing

`index.html` is the only file to edit — it's both the source and the deployed
page. Inside the `<script type="text/x-dc" data-dc-script>` block near the
bottom:

- `this.data` — the project list (title, summary, tag, stack, repoUrl, etc.)
  shown in Featured Projects / All Projects / case-study pages.
- `this.jobs` — work experience entries.
- `this.i18n` — English/Thai/Burmese copy.

## Running locally

```bash
python3 -m http.server 8765
# open http://localhost:8765/index.html
```

## Deployment

Push to `main` — GitHub Pages serves directly from the repo root. DNS for
`thantzinmin.tech` points at GitHub Pages (A/AAAA records + this repo's
`CNAME` file).
