# Naresh Goud Boddu — academic homepage

A clean, fast, single-page academic website. Plain HTML + CSS, no build step,
no dependencies. Loads instantly and works on any host.

```
naresh-website/
├── index.html          ← all content lives here
├── assets/
│   ├── style.css       ← all styling
│   ├── profile.jpg     ← ADD: your headshot (square, ~600×600px)
│   └── cv.pdf          ← ADD: your CV (optional)
└── README.md
```

## Add your photo and CV

1. Drop a square photo at `assets/profile.jpg` (the hero hides gracefully if missing).
2. Drop your CV at `assets/cv.pdf` (or remove the "CV (PDF)" link in `index.html`).

## Preview locally

Just open `index.html` in a browser, or serve it:

```bash
cd naresh-website
python3 -m http.server 8000   # then visit http://localhost:8000
```

## Deploy to GitHub Pages

**Option A — user site at `https://<username>.github.io` (recommended):**

```bash
cd naresh-website
git init -b main
git add .
git commit -m "Initial academic homepage"
# create an EMPTY repo on GitHub named exactly:  <username>.github.io
git remote add origin https://github.com/<username>/<username>.github.io.git
git push -u origin main
```

Your site goes live at `https://<username>.github.io` within a minute or two.

**Option B — project site:** push to any repo, then in the repo go to
*Settings → Pages → Build and deployment → Source: Deploy from a branch →
`main` / `root`*. Site appears at `https://<username>.github.io/<repo>`.

## Custom domain (optional)

Buy a domain (e.g. `nareshboddu.com`), then:

1. Add a file named `CNAME` containing just your domain (e.g. `nareshboddu.com`).
2. At your DNS registrar, add `A` records pointing to GitHub's IPs
   (`185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`)
   and a `CNAME` for `www` → `<username>.github.io`.
3. In *Settings → Pages*, set the custom domain and enable "Enforce HTTPS".

## Editing content

Everything is in `index.html` — sections are clearly commented
(`<!-- NEWS -->`, `<!-- PUBLICATIONS -->`, etc.). To add a publication, copy an
existing `<div class="pub">…</div>` block and edit it. Colors and fonts are
CSS variables at the top of `assets/style.css`.

## Verify before going public

A few links use best-guess URLs based on your current site — please confirm:
- Google Scholar profile URL
- arXiv author page
- DBLP author page
- LinkedIn handle
