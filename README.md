# Lietuva.AI — Landing Page

A single-page threshold for **lietuva.ai**. Modeled on palarchive.org: full-bleed archival artifact, minimal type, "Enter the Archive" link.

## Files

```
lietuva-ai-landing/
├── index.html      — single self-contained page
├── hero.jpg        — austinis textile background (3.5 MB)
├── vercel.json     — static deploy config + caching
└── README.md       — this file
```

## What it does

- Background: woven `austinis` textile from Žiburio Archyvas
- Brand mark top-right: "Lietuva.AI / CultureNet Pilot"
- Centered title: serif "Lietuva.AI" + bilingual EN/LT tagline
- Bottom-center link: **Enter the Archive · Įeiti į archyvą** → `https://archyvas.ziburioltmokykla.org`
- Footer ribbons: "Phase I — Žiburio Archyvas" / "A CultureNet Initiative"

When more archives connect (Phase II+), this page becomes a portal hub — for now, single Enter link.

## Local preview

```bash
cd ~/LietuvaAi-CultureNet/lietuva-ai-landing
python3 -m http.server 8765
# open http://localhost:8765
```

Or just double-click `index.html` — Google Fonts will load over network, the rest is self-contained.

## Deploy to lietuva.ai (Vercel)

1. Push this folder to a new GitHub repo (`lietuva-ai-landing`)
2. Import in Vercel → framework: **Other** (no build step)
3. Output dir: `./` (root)
4. In Vercel project → Settings → Domains → add `lietuva.ai` and `www.lietuva.ai`
5. Update DNS at your registrar:
   - `lietuva.ai` → A record `76.76.21.21`
   - `www.lietuva.ai` → CNAME `cname.vercel-dns.com`

## When Phase II archives are added

Replace the single `<nav class="enter">` block with a small grid of archive cards, each linking to its own subdomain. The hero, brand mark, and meta footers stay.
