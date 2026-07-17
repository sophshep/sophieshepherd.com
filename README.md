# sophieshepherd.com

Personal site — a single static `index.html` with an optimized photo. No build step, no dependencies.

## Structure
- `index.html` — the whole site (inline CSS + a tiny copy-email script)
- `profile.jpg` — optimized profile photo (~33 KB)
- `CNAME` — custom domain for GitHub Pages
- `.nojekyll` — serve files as-is (skip Jekyll)

## Deploy (GitHub Pages)
1. Push this folder to a **public** repo on GitHub.
2. Repo → **Settings → Pages** → Source: **Deploy from a branch** → `main` / `/ (root)`.
3. Under **Custom domain**, `sophieshepherd.com` is picked up from the `CNAME` file. Enable **Enforce HTTPS**.
4. At your DNS registrar, point the domain at GitHub Pages:
   - Apex `sophieshepherd.com` → four `A` records: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - (optional) `www` → `CNAME` to `<username>.github.io`

## Local preview
Just open `index.html` in a browser, or run `python3 -m http.server` in this folder.
