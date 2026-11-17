# Nadirix Flow — Landing Site

The public-facing front door for the Nadirix Flow project — a local-first household AI and operations platform.

**Live domain:** [nadirix-flow.cc](https://nadirix-flow.cc)  
**Documentation:** [docs.nadirix-flow.cc](https://docs.nadirix-flow.cc)  
**GitHub:** [Krazy-Killa/Nadirix-Flow](https://github.com/Krazy-Killa/Nadirix-Flow)

## Tech Stack

- [Astro](https://astro.build) — static site generator
- Pure CSS — no framework dependencies
- Cloudflare Pages — hosting & deployment

## Development

```bash
npm install
npm run dev      # local dev server at http://localhost:4321
npm run build    # production build to ./dist
npm run preview  # preview the production build
```

## Deployment (Cloudflare Pages)

1. Push this repo to your GitHub.
2. In the Cloudflare dashboard, go to **Workers & Pages → Create → Pages → Connect to Git**.
3. Select the repository and set:
   - **Build command:** `npm run build`
   - **Build output directory:** `dist`
4. Deploy. Cloudflare will auto-build on every push.
5. Add a custom domain (`nadirix-flow.cc`) under **Pages → Custom domains**.

## Structure

```
src/
├── layouts/
│   └── Layout.astro       # HTML shell, meta tags, global styles
├── components/
│   ├── Nav.astro           # Fixed top navigation
│   ├── Hero.astro           # Landing hero with CTAs
│   ├── Features.astro       # Capability cards
│   ├── DevelopmentJourney.astro  # Maturity / roadmap
│   ├── QuickStart.astro     # 5-step overview + terminal
│   ├── LinksHub.astro       # Resource link cards
│   └── Footer.astro         # Footer with links
├── pages/
│   └── index.astro          # Main page assembling all sections
└── styles/
    └── global.css           # Theme tokens, grid bg, glass panels
```

## Theme

| Token | Value |
|-------|-------|
| Background | `#080c12` |
| Primary panels | `#0e151e` |
| Raised surfaces | `#131e2a` |
| Accent | `#42f5c5` |
| Primary text | `#e9f1f5` |
| Secondary text | `#8295a4` |

Fonts: Space Grotesk (headings), Inter (body), JetBrains Mono (technical/code).
