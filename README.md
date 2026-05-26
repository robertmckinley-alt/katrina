# Katrina's Genetic Story — Website

An interactive, friendly genetic report built from a 23andMe v5 raw-data file and a
5.5-year personal pain & hormone diary. It's a single self-contained file: **`index.html`**
(no build step, no dependencies, works offline).

> Educational only — not medical advice, not a diagnosis.

---

## View it right now

Just **double-click `index.html`** — it opens in any web browser and works fully offline.

---

## Put it online with Git + Vercel

I built the site and set up a Git repository for it, but this workspace has **no internet
access to Vercel**, so the final "go live" step has to run from your own computer. It takes
about 2 minutes. Pick whichever option you like.

### Option A — Vercel CLI (fastest)

```bash
# 1. install the Vercel command-line tool (needs Node.js)
npm install -g vercel

# 2. go to the folder that contains index.html, then:
vercel            # first run opens a browser to log in, then deploys a preview
vercel --prod     # publishes the production site and prints the live URL
```

When asked, accept the defaults. Framework Preset = **Other**. No build command needed.

### Option B — Git + GitHub + Vercel (uses Git, auto-deploys on every change)

```bash
# in the folder that contains index.html and README.md:
git init
git add .
git commit -m "Katrina's Genetic Story - interactive genetic report"
git branch -M main

# create an empty repo at github.com, then:
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

Then on **vercel.com → Add New → Project → Import** your GitHub repo → **Deploy**.
After that, every `git push` updates the live site automatically.

---

## Settings that matter

- **Framework Preset:** Other (it's a plain static site)
- **Build Command:** none
- **Output Directory:** leave default (the repo root)
- The site will be served at a `https://<name>.vercel.app` address.

## Privacy note

This page contains Katrina's name, genetic results and health context. A normal Vercel
URL is **public** (though the address is random and the page already includes a
`noindex` tag so search engines skip it). If you'd like it truly private, Vercel offers
**Password Protection / Deployment Protection** in the project settings — worth turning
on for personal health information.
