# Tasfia Tasnim — Portfolio

Personal portfolio site for Tasfia Tasnim, a full-stack developer working with React, FastAPI, and SQL. Live at: https://tasfiatasnim18.github.io/Tasfia-Tasnim-Portfolio/

## About

A single-page portfolio built around a "systems monitor" visual identity — inspired by the Clinical Decision Support System thesis project featured on the site. No frameworks, no build step: everything is a single self-contained HTML file with inline CSS and JavaScript.

**Sections:** Home · About · Skills · Flagship Project (CDSS) · Experience · Education · Contact

## Stack

- HTML5, vanilla CSS (custom properties for theming), vanilla JavaScript
- Fonts: [Space Grotesk](https://fonts.google.com/specimen/Space+Grotesk), [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono), [Inter](https://fonts.google.com/specimen/Inter) — loaded via Google Fonts
- No dependencies, no package manager, no build tools

## Features

- Light/dark mode toggle (respects system preference, persists choice via `localStorage`)
- Fully responsive, down to mobile
- Keyboard-accessible with visible focus states
- Scroll-triggered section reveals (`IntersectionObserver`)
- Open Graph / Twitter card meta tags for clean link previews when shared

## Repo structure

```
tasfia_tasnim_portfolio/
├── index.html          # entire site — markup, styles, and scripts
├── cv/
│   └── Tasfia-Tasnim-CV.pdf   # downloadable CV, linked from the hero button
└── README.md
```

## Running locally

No build step required. Either:

- Open `index.html` directly in a browser, or
- Serve it locally for a closer-to-production feel:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deployment

Hosted on **GitHub Pages** from the `main` branch. Any push to `main` updates the live site automatically — no CI/CD configuration needed.

## Updating content

Everything lives in `index.html`:

- **Profile info, bio, stats** — `<section id="home">` and `<section id="about">`
- **Skills** — `<section id="skills">`, grouped into panels by category
- **Flagship project** — `<section id="project">`
- **Work experience** — `<section id="experience">`
- **Education** — `<section id="education">`
- **Contact details / form** — `<section id="contact">`

To swap the CV file, replace `cv/Tasfia-Tasnim-CV.pdf` with the new PDF (same filename), or update the `href` on the "Download CV" button in the hero section if the filename changes.

## License

Personal project — all rights reserved.
