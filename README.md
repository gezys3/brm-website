# AI Capabilities & SME Resilience — BRM Group Website

Single-page research website for the Business Research Method group project.

## Structure

```
brm-website/
├── index.html              <- the entire site (HTML + CSS + JS in one file)
├── README.md
└── assets/
    └── img/
        ├── hero.jpg        <- homepage banner
        ├── lecturer.jpg    <- add
        ├── member1.jpg     <- add
        ├── member2.jpg     <- add
        ├── member3.jpg     <- add
        └── member4.jpg     <- add
```

## Adding photos

Drop the files into `assets/img/` using the exact names above.
See `assets/img/PUT-PHOTOS-HERE.txt` for the name → person mapping.
Missing photos fall back to the person's initials, so the site never breaks.

## Viewing locally

Double-click `index.html`, or for an accurate preview:

```bash
cd brm-website
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploying

The site is fully static — no build step, no dependencies.

**Netlify Drop** — drag the `brm-website` folder onto https://app.netlify.com/drop

**GitHub Pages**
```bash
git init && git add . && git commit -m "BRM group website"
git branch -M main
git remote add origin <your-repo-url>
git push -u origin main
# Repo Settings > Pages > Source: main branch, / (root)
```

**Vercel** — `npx vercel` from inside this folder.

Any static host works; just upload the folder and keep `index.html` at the root.

## Content

- **Home** — background of study, conceptual chain, lecturer and group members
- **Chapter 1** — problem statement, objectives, questions, hypotheses, scope
- **Chapter 2** — Dynamic Capabilities Theory, variables, conceptual framework
- **Chapter 3** — methodology, data collection, PLS-SEM results, bootstrapping

Diagrams are inline SVG, so they stay sharp at any zoom and need no image files.
