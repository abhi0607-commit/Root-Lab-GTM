# ROOT LAB — From Research to Market

An interactive case-study site for **ROOT Lab**, a *simulated* student trade project: a research-informed scalp-care concept and a proposed US market-entry strategy.

> **Group Project: Simulated Market strategy case study.** ROOT Lab is a provisional company name. Nothing was manufactured, tested, launched, sold or exported. No supplier, buyer, retailer or influencer agreement exists. All numbers come from the team's research notes, and modeled figures are labelled as such.

## Run it

```bash
npm install
npm run dev       # local dev server (http://localhost:5173)
npm run build     # type-check + production build into dist/
npm run preview   # serve the built site (http://localhost:4173)
```

Stack: Vite 5, React 18, TypeScript (strict), Tailwind CSS 3, Framer Motion, Recharts. Fonts (Inter, Fraunces) are bundled locally through Fontsource. There's no backend, analytics or external request.

## What's on the site

Ten sections, viewable as a scrolling case study or in **Present** mode (`←` `→` `Home` `End`, clickable stepper, progress bar). The chosen mode is remembered for the browser session only.

1. Cover
2. What we investigated (four expandable workstreams)
3. Consumer concerns vs Google search interest (two separate charts)
4. Five-competitor explorer (brand filter, list/table toggle, source side panel)
5. Cross-product review patterns (n = 36, paraphrased, no frequencies)
6. Proposed product experience (hotspots, issue → response flip)
7. Why the US was selected (source scores + live weighting tool)
8. Export-cost simulator (editable inputs, reset, stacked breakdown, exclusions, compliance checklist)
9. Proposed go-to-market (4P tabs, buyer screening flow, SWOT/TOWS)
10. Summary (key figures and what the project did)

The site honours `prefers-reduced-motion` and works without animation.

## Data provenance

| Source | Status | Used for |
|---|---|---|
| `Group A Trade Project Notes_.pdf` (111 pages) | **Used** (found in `Downloads/`, not in this folder) | Every number and claim on the site |
| `ROOT_LAB_site_data.json` | **Missing** | Not used. The equivalent data was transcribed from the PDF into `src/data/` |
| `ROOT_LAB_Interactive_Portfolio_10_Slides.pptx` | **Missing** | Not used. Section order follows the build brief |
| Four ROOT Lab mockup images | Used | Originals copied to `assets/`; resized WebP copies in `public/assets/` |

Page references (kept in `src/data/`, no longer shown on the site) are **physical PDF page indices (1-based)**. Google Trends values (pp. 81–85) were parsed straight from the PDF text, not typed by hand, and the duplicate itchy-scalp table on pp. 86–87 matches exactly.

### Checked against the source
- Survey: 45 / 41 / 30 / 24 / 24 / 13 % of **surveyed US women**, preceding six months (p. 102).
- Competitors: exactly five; selected reviews 7 + 6 + 6 + 7 + 10 = **36** (pp. 97–100).
- Market scores: US 87, EU 72 (region), Japan 70, China 65, Vietnam 48. Recomputing with the p. 62 weights reproduces all five exactly.
- Landed cost: 10,000 units → **$73,582.84**, **$7.36/unit** (p. 79), computed live rather than hard-coded.

## Where to edit

| What | File |
|---|---|
| Section list, working name | `src/data/project.ts` |
| Survey / Trends | `src/data/survey.ts`, `src/data/trends.ts` |
| Competitors / review themes | `src/data/competitors.ts`, `src/data/reviews.ts` |
| Market criteria and scores | `src/data/market.ts` |
| Landed-cost defaults and exclusions | `src/data/cost.ts` (calculations in `src/lib/calc.ts`) |
| Fact check, conflicts, unverified items | `src/data/integrity.ts` |
| Section copy and layout | `src/sections/*.tsx` |
| Colours and fonts | `tailwind.config.js`, `src/index.css` |

## Deploying (not done)

The build output in `dist/` is a static site with relative paths, so it can be hosted anywhere. **It has not been deployed.**

- **Netlify:** drag the `dist/` folder into app.netlify.com/drop, or connect a repo with build command `npm run build` and publish directory `dist`.
- **Vercel:** import the repo; framework preset "Vite", build `npm run build`, output `dist`.
