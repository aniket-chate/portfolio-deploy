# Aniket Chate — Portfolio (Static Site)

Plain HTML/CSS site, no build step, no server needed. Just `index.html`,
`style.css`, and an `images/` folder.

## Before you deploy

1. Drop your real images into `images/` following the exact paths/names
   listed in `images/README.txt` (case-sensitive!).
2. Delete `images/README.txt` and the `.gitkeep` files once real images are
   in place (optional — harmless if you leave them).
3. Open `index.html` directly in a browser to confirm everything renders
   and no images are broken before pushing anywhere.

## Deploy option 1: GitHub Pages (free, recommended)

1. Create a new **public** repo on GitHub (e.g. `portfolio`).
2. From inside this folder:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Build and deployment → Source** → select
   `Deploy from a branch` → Branch: `main`, folder: `/ (root)` → **Save**.
4. Wait ~1 minute, then your site is live at:
   `https://<your-username>.github.io/<repo-name>/`

## Deploy option 2: Netlify (free, drag-and-drop, no git needed)

1. Go to https://app.netlify.com/drop
2. Drag the whole `portfolio-deploy` folder onto the page.
3. Netlify gives you a live URL instantly (e.g. `random-name.netlify.app`).
4. Optional: claim a nicer subdomain or connect a custom domain under
   **Site settings → Domain management**.

## Deploy option 3: Vercel

1. `npm i -g vercel` (one-time), then run `vercel` inside this folder and
   follow the prompts — or import the GitHub repo at https://vercel.com/new
   for automatic redeploys on every push.

## Custom domain (optional, any host)

If you buy a domain (Namecheap, GoDaddy, etc.):
- **GitHub Pages:** add a `CNAME` file containing your domain, then point
  your domain's DNS to GitHub's IPs (GitHub's Pages settings page shows the
  exact records to add).
- **Netlify/Vercel:** add the domain in the dashboard; they'll show you the
  DNS records to add at your registrar.

## Common issues

| Symptom | Fix |
|---|---|
| Images broken after deploy | Check `images/` folder was actually pushed, and filenames match case exactly |
| Site shows folder listing instead of your page | File must be named `index.html`, not `portfolieo.html` |
| Fonts not loading | Confirm you have internet access to Google Fonts (no local fix needed — the `<link>` tags handle it) |
| Changes not showing after push | GitHub Pages can take 1–2 min to rebuild; hard-refresh (Ctrl/Cmd+Shift+R) |
