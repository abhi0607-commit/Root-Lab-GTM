# Claude Code — build instruction: ROOT LAB | From Research to Market

You are a senior interactive frontend engineer, motion designer, evidence-conscious data storyteller and accessibility reviewer. Build a **production-quality, responsive interactive portfolio case-study site** for ROOT LAB. The final result should look like a credible premium brand strategy presentation crossed with an interactive market-intelligence report—not an online shop and not a generic template.

## FIRST: inspect the actual assets

Before modifying files, inspect these files in the working folder:

1. `ROOT_LAB_Interactive_Portfolio_10_Slides.pptx` — the **story order, slide design, and speaker notes**.
2. `Group A Trade Project Notes_.pdf` — original **111-page research source**.
3. `ROOT_LAB_site_data.json` — exact curated data, citations and qualifications.
4. `assets/` — the four user-supplied ROOT Lab product images.

Do not claim to have inspected files you have not opened. Do not make up any missing data. If a file is absent, say which one is missing and build only from the other available sources. Prioritize the **original PDF for factual statements**, then the JSON for the curated website dataset, then the PowerPoint for presentation structure. If two sources conflict, **do not silently choose one**. Expose the conflict under a “Research notes / limitations” popover or use cautious, clear wording.

## Project truth rules: non-negotiable

This is a **SIMULATED PROJECT**. ROOT Lab has not been verified as a registered business or as having manufactured, tested, clinically validated, launched, sold, exported, generated revenue, secured a retailer, hired influencers, run ads, signed a distributor, performed real consumer interviews, or obtained FDA approval. No sales or conversion KPIs exist. Use “proposed”, “modeled”, “research-informed”, “working concept”, “estimated”, or “would” where appropriate. Don't repeatedly clutter every line with disclaimers: put a visible project-status tag at the top and precise labels beside modeled/uncertain data.

- **No fabricated citations, screenshots, consumer quotes, contact names, product photos, profit margins, forecasts, importer relationships or outcomes.**
- **Keep exactly five named competitor products:** medicube Rosemary PDRN Scalp Serum; VT PDRN Reedle Shot Brush Hair Serum; Lilyeve Grow:Turn Exosome Brush Ampoule; Lilyeve Scalp:Turn Cica PDRN Brush Ampoule; Seapuri Scalpy Hair Serum.
- The **36 review entries** are a selected exploratory sample, distributed 7, 6, 6, 7, 10 respectively. A Lilyeve Scalp:Turn review may refer to shampoo. Do not claim the entire sample was fully validated or representative. Never invent theme frequencies.
- The **45% itchy scalp** is a **survey percentage**, attributed in the source notes to surveyed US women who reported the concern over the prior six months. It is **not** a Google Trends increase or a percentage of all Americans. Other survey values from the source are 41% dry scalp, 30% flaking/dandruff among surveyed women, 24% oily scalp, 24% buildup, 13% irritation. Survey sample size and fieldwork date aren't documented in the notes.
- The Google Trends data in the PDF lists **Dec 2022–Nov 2026** monthly index values. The source lacks export date, geography and search settings. November 2026 is incomplete as of Nov 24, 2026. Chart only values directly transcribed from the source PDF. Indexed search interest is **0–100, never %**. Never infer a growth rate from the 45% survey figure.
- Country ranking source reports **United States 87**, **EU 72**, **Japan 70**, **China 65**, **Vietnam 48** out of 100. These are **team-weighted attractiveness assessments**, not measured commercial outcomes. The **EU is a region**. The raw criteria and weights in `ROOT_LAB_site_data.json` can be used for an interactive **recomputed** weighted ranking, but the recomputed result must be labeled separately if it differs from the PDF-reported scores. Do not silently rewrite source scores.
- Export economics: **10,000 units, $60,000 assumed factory cost, $73,582.84 modeled landed cost, ~$7.36 per unit**. The 12.5% duty is an **assumption from project notes** for this scenario—not a live rate quote. No verified supplier invoices or profit figures; retail platform fees, ads and returns are excluded.
- Product name: use **Reedle Shot Scalp Barrier Recovery Ampoule** as the **working name** because it appears as a “final selection” in the brand-identity section (PDF p. 36); acknowledge other draft names exist. Its **formulation is proposed** and no product efficacy is demonstrated. Do not represent a finalized INCI, “non-irritating” lab result, clinical data or compatibility with minoxidil.
- References to US cosmetics classification, FDA/MoCRA, labeling and trade rules in the PDF are **research notes**. Add “Verify applicable current rules before a real import” rather than claiming legal clearance.
- Buyer companies in the notes are **candidates**, not partners. Do not present unverified names as certified importers or confirmed buyers.
- Do not call the SWOT/TOWS project findings operational results. Explain the strategic framework briefly, but avoid filler interpretations and exaggerated “white space proven” claims.
- Do not invent the portfolio owner's individual contributions. Include a **“My Role” editable placeholder** requiring user input, or omit from published view until completed.

## Build stack, output and quality

Create a complete **Vite + React + TypeScript + Tailwind CSS** application. Install needed dependencies and ensure `npm run dev`, `npm run build`, and `npm run preview` actually work. Use **Framer Motion / Motion for React** for transitions; use Recharts or equivalent for charts and a lightweight CSS or SVG cost breakdown. No backend, login, database, external analytics, fake API calls or fabricated real-time metrics. Ship a **complete README**, `package.json`, and organized `src/` with typed data definitions, small reusable components and accessible control states. Use assets locally, not remote stock imagery.

The site must also be readable and complete **without** animations; honor `prefers-reduced-motion`. Optimize performance and accessibility: responsive 320px to desktop; keyboard navigable; high contrast; alt text; semantic landmarks; focus styles; logical heading hierarchy. Avoid hijacked scrolling and parallax-induced motion sickness. Charts require textual summary and data source beneath.

## Visual language

- Art direction: premium Korean beauty, editorial consulting case study, not flashy ecommerce.
- Brand palette: Aubergine `#48203F`, muted plum `#744C6B`, warm ivory `#F7F2EC`, pale rose `#EFE2EA`, soft sage `#B7BE9E`, ink `#25242A`.
- Typography: a readable modern sans-serif for body and strong editorial display serif/sans for headings. Keep captions legible (at least 12–13 CSS px), body 16–18px. Avoid thin or tiny text.
- Beautiful generous whitespace; one strong point per section; limited purposeful animations.
- Use the actual four ROOT Lab images in `/assets`; never replace them with invented product renders or random stock photos. Preserve their labeling. A product mockup is evidence of design exploration, not production.
- Headline: **ROOT LAB — From Research to Market**. Do **not** put “Built for the U.S.” in the hero.

## Navigation and motion (genuine working interactions)

Build a presentation-mode toggle with 10 step sections, keyboard controls (`←`, `→`, `Home`, `End`, with appropriate focus handling), clickable side stepper and persistent progress indicator. In normal mode, the page becomes a scrollable case study with anchor links. Persist mode only in current session if easy; don't assume storage needed. Add smooth, subtle 220–450ms slide entrance, chart reveal and image transform, with reduced-motion fallback. Make the site compelling even on a static screenshot.

### Section 1 — Cover

Hero ROOT LAB / From Research to Market. Subheading: “A research-informed scalp-care concept and simulated US market-entry strategy.” Show project status “Simulated strategy case study”, one prominent original product image, a button that actually navigates to the next section, and brief methodology chips: research / product / trade / marketing.

### Section 2 — What we investigated

Four linked steps: consumer & competitor research → product concept → US market and economics → proposed promotion and buyer discovery. Each step expands on tap/click with **2–4 sentences**, evidence tags (“Research”/“Proposed”/“Modeled”), and page references. Do not invent research operations that are absent from the PDF.

### Section 3 — Consumer concerns vs Google Search Interest

Use a real horizontal bar chart for the **survey percentages** from `ROOT_LAB_site_data.json` with the clear denominator label “surveyed US women” and “reported concerns in preceding six months.” Tooltip also states original fieldwork dates and survey sample size are not documented. On the other side, a **separate** Trends timeline if the actual values can be extracted and validated from the PDF. Explicit label “search-interest index (0–100)” and period Dec 2022–Nov 2026; note source export settings are unknown and Nov 2026 was incomplete. If series cannot be reliably transcribed, present a source-scope note and DO NOT draw an invented line chart. Implement a simple info control describing why these datasets must not be compared as like units.

### Section 4 — Five competitor explorer

Cards for the five precise competitor names and selected-review counts. Provide filters by brand, and toggle between product list and data table. Show only specifications with a verified source in the PDF; missing price, format, ingredients, current listings or product photos must say “Not verified in project notes.” Display selected review count (not customer population or volume sold). Cards open a side panel with source-page citations and limitations. If external product images were not supplied, use typographic cards (not fabricated packs).

### Section 5 — Cross-product review patterns

Five interactive thematic rows: texture/residue; applicator convenience/dispenser friction; comfort/cooling and potential irritation; value/volume; uncertainty about visible results. On click show a **paraphrase of documented selected reviews** from PDF pages 97–101, tagged by product when supportable. Do not invent direct quotes. The section should visibly state `n=36 selected reviews; exploratory; one uncertain product match`. No fake theme-frequency bar or word cloud.

### Section 6 — Proposed product experience

Use brand product visuals, interactive hotspots for PDRN / Cica Reedle™ idea, scalp hydration/comfort supporting ingredients, applicator concept and texture target. Add simple flip between “Consumer issue in research” and “Proposed ROOT Lab design response.” All product specs are concepts; avoid “clinically proven”, “treats hair loss”, “non-irritating”, “FDA approved”, “revolutionary” or definite efficacy statements. Include exact working product name and p. 36 citation. Clearly say design target rather than tested performance.

### Section 7 — Why the US was selected

Show source-reported ranking with scores: 87,72,70,65,48. Below, a **real interactive weighting tool** using the eight criteria from JSON. Visitors can adjust sliders and reset weights to source defaults. Normalize weights to sum to 100 for comparison and use formula `sum(weight_i * score_i / 5)`; document the method. Show both **source-reported baseline** and **live recalculated scenario** as separate labelled views, and note any mismatch clearly. Don't pretend this score is evidence of realized market demand.

### Section 8 — Export-cost simulator and trade lens

Default inputs exactly match the source's itemized 10,000-unit model. Editable shipment units, assumed factory unit cost, freight, packing, insurance, tariff rate, MPF, HMF, brokerage and US delivery. Calculate total and per-unit landed cost with correct arithmetic. Add “Reset to project model” button. Show a stacked bar with detailed breakdown and a **full list of excluded costs**. If cost formula changes assumptions, label clearly as a new user-adjusted scenario. Add an expandable customs/compliance checklist referencing working HS 3305.90, cosmetic-vs-drug positioning, FDA/MoCRA, labeling, and importer-of-record due diligence. No false compliance certification and no live tariff claims.

### Section 9 — Proposed go-to-market

Four interactive columns Product / Price / Place / Promotion. Price hypothesis $25–28 per 100 mL (not actual selling price). Place: proposed Amazon US/DTC first and B2B candidates later; no confirmed agreements. Promotion: short-form demo videos, beauty creators, education and sampling **ideas**, not executed campaigns. Add buyer screening flow: discover → legal identity → relevant imports → category / channel fit → proposed tier ranking. Clearly distinguish proposed retailer channels from signed partners. Include mini SWOT/TOWS rationale sourced to PDF pp. 38–41 without claiming a competitive advantage was empirically proven.

### Section 10 — Summary / research integrity

Summarize precisely: five named competitors, 36 selected reviews, US scoring 87/100, proposed scalp ampoule, modeled landed cost $7.36, and prospective digital-first market entry. Show “What this project did” vs “What was not executed” in an elegant expandable fact-check panel. Include a small “Methods & Sources” drawer with original PDF page labels and a brief section for unverified details: survey fieldwork/sample, selected review-match issue, Trend export settings, market value definitions, hypothetical quote and tariff, and buyer validation. Use a lightweight editable “My contributions” placeholder rather than inventing team roles.

## Source provenance in UI

Every main graphic and numerical claim must have an unobtrusive source footer such as `Source: Group A Trade Project Notes, p. 62`. For sources cited only inside the PDF, say `as cited in project notes`; never pretend an external publication was directly checked. Include a `Source & uncertainty` popover per major section with precise source pages. Keep source page numbers as physical PDF page indices (1-based), not guessed page labels.

## Data and interactions acceptance tests

At minimum, implement and verify:

1. All 10 sections are navigable by keyboard, clicks and presentation/scroll toggles.
2. Every original asset loads; no 404s or stock images.
3. Five competitors exactly match the list above; review counts total **36**.
4. Survey chart values are **45/41/30/24/24/13**, correctly attributed; **never** labelled Trends percentage.
5. Market source scores read **87/72/70/65/48**; scenario sliders recalculate and reset. The EU is described as a region.
6. Cost reset gives **$73,582.84** for **10,000** units and approximately **$7.36** per unit. Changing quantity or duty updates computed outputs without hard-coded labels.
7. No fabricated graph series, review quotes, legal certification or sales KPI.
8. Mobile and desktop have no overflow, overlapping panels, invisible text or broken navigation.
9. Reduced-motion users see the same content without elaborate transitions.
10. `npm run build` completes successfully, with no TypeScript errors.

## Deliverables

Provide the complete working project files, not just pseudocode. Explain exact commands: `npm install`, `npm run dev`, and `npm run build`. Produce a short README explaining project simulation status, original PDF/data provenance, known research limitations, where to edit copy/data, and how to deploy a static site (e.g. Vercel or Netlify) without claiming deployment has happened.

Finally, self-review every section against the original PDF for source alignment, especially: slide 3 survey vs Trends; slide 4 five-competitor identity and n; slide 7 weighted scores; slide 8 duty and $73,582.84; and statements about manufacturing or results. If any detail is unclear, show “Not verified in source” rather than inventing it. **No filler, no unsupported superlatives, no fake quantitative impact.**
