# Gurujit Enterprises — Design Brief (Phase 0)

## Design read
For government engineers, municipal officers, and contractors in Odisha evaluating a civil-infrastructure partner. Emotional register: engineered, trustworthy, heavy — the calm authority of poured concrete and a finished highway at blue hour.

## Concept spine
"From survey to asphalt." The page is a living engineering drawing that builds itself: crosshairs, chainage markers, measurement annotations and a blueprint grid resolve into real roads, flyovers and drainage works. The visitor orbits a piece of infrastructure like a site engineer walking the job.

## Delivery tier
SPECTACLE — the user explicitly asked for a 3D portfolio with both an interactive 3D hero scene and motion effects. Cinema base + WebGL/3D hero + custom cursor + a second mid-page beat.

## Locked palette — "Asphalt Blueprint"
Dark, blue-undertoned (NOT neutral graphite) with warm concrete bone text and a single road-sign yellow accent. Derived from the material world: night-lit highway, blueprint ink, poured concrete, hi-vis signage.
- `--ink`     `#0A1622` — deep asphalt blue-black (ground; blue chromatic cast, not graphite)
- `--surface` `#0F2138` — deep cobalt panel / elevated card
- `--surface-2` `#16304E` — lighter cobalt line/edge
- `--bone`    `#D8D1C2` — warm concrete bone (primary text)
- `--bone-dim` `#8A93A1` — muted slate (secondary text)
- `--signal`  `#E8B820` — single road-sign yellow accent (CTAs, survey markers, active states)
- `--paper`   `#E7E1D3` — concrete paper (light section ground)
Defense: amber-on-graphite (banned family #1) is replaced by a blue-black ground + a golden road-sign yellow that reads as construction signage, not ember. No neon glow (banned #2), no beige+brass (#3), no purple (#4).

## Locked type
- Display + body: **Satoshi** (geometric grotesk, engineered/precise feel; via Fontshare).
- Mono: **JetBrains Mono** (chainage, coordinates, elevations, stats, survey annotations; via Google Fonts).
Inter-as-display is banned; Satoshi carries more character and fits engineering precision. No serif — this is a technical/engineering brand, not editorial luxury.

## Corner / border language
Sharp. Hairline rules (`1px solid var(--surface-2)`), 0–2px corner radius on the rare card, blueprint grid lines. One corner scale page-wide: sharp. No soft rounded pills, no mixed radii.

## Tier-1 technique (wow-catalog B3 — 3D subject scene)
Approved hero image (a dramatic highway flyover / elevated interchange ramp at blue hour, single clean structure) → `higgsfield_generate_3d` → R3F scene with scroll-driven camera orbit + cursor tilt. The visitor rotates the structure by scrolling and nudges the camera with the cursor, exactly as a surveyor walks a flyover. Defense: the spine is "survey to asphalt" — orbiting the structure enacts the site engineer's walk-around.
Robust fallback if the GLB is weak: B1 cutout-parallax rig (same hero subject cut from its plate, layered depth on scroll + cursor). Decide after the GLB lands.

## Second beat (spectacle)
D1 — Horizontal cinema rail for the Projects section: a pinned section pans horizontally through a wide panorama of project plates (roads, flyovers, drainage, government buildings). The scroll-axis rotation is the surprise.

## Custom cursor (spectacle tier)
A surveyor's crosshair that snaps/scaling toward interactive elements; reduced-motion = default system cursor.

## Section plan (7 sections, 7 distinct layout families, no consecutive repeats)
1. HERO — full-bleed R3F 3D scene (flyover GLB, cursor-tilt + scroll-orbit) behind a bottom-left scrim with headline + subtext + CTA row. Architecture: massive image-first / asymmetric (NOT left-text/right-image).
2. STATS — full-width metric strip (km of roads, projects delivered, years operating, govt tenders executed), JetBrains Mono numerals, hairline-divided, oversized metrics. Eyebrow: none.
3. ABOUT — editorial offset / asymmetric zigzag: who Gurujit Enterprises is (civil construction, govt tenders, roads & infrastructure, all Odisha) beside a construction-site plate. Mid-page left-text/right-image (the one allowed use).
4. SERVICES — asymmetric bento (6 cells, varied sizes): Road construction, Earthworks & grading, Bridges & culverts, Drainage & RCC, Government tendering, Site development.
5. PROJECTS — horizontal cinema rail (D1 second beat): pinned, pans through wide project panorama plates.
6. PROCESS — vertical timeline / sticky-stack with hairline rules + mono step markers: Survey & feasibility → Design & estimation → Tender & procurement → Execution → Quality & handover.
7. CONTACT — split: left contact info (both phones, Bhatti Road Birmitrapur address, all-Odisha service area, hours), right enquiry form. Server function receives the enquiry.

Eyebrow budget: ceil(7/3) = 2. Use at most 1 eyebrow total; let headlines carry.

## CTA inventory (bespoke chrome — each its own component, own interaction identity)
1. Hero primary — "Start your project" — survey-crosshair garment: a corner-bracket target (viewfinder) that closes around the label on hover; fills signal-yellow on active.
2. Hero secondary — "Call 99370 09220" — mono underlined inline-link, arrow travels along a drawn route line on hover. Phone intent.
3. Projects — "Explore projects" — oversized numeral/glyph hit area as the link caption; row shears/shifts grade on hover. Browse intent.
4. Contact form submit — "Send enquiry" — stamp/press garment: :active imprints (skew + texture shift). Submit intent (distinct from contact intent).
No site-wide `.btn` utility classes. Each styled in its own component.

## Asset plan (asset-system.md)
- Hero visual: 2 candidates (flyover/interchange at blue hour, single clean structure suitable for 3D); pick one; interaction pair optional.
- 3D subject: hero → GLB (spectacle).
- Section plates: 2–3 atmospheric backdrops (asphalt texture macro, concrete macro, blueprint grid, dust/atmosphere) for section grounds.
- Content imagery: construction-site plate (about), 4 project plates (roads/flyover/drainage/govt building), process step spot illustrations (optional).
- Custom icon set: 6–8 glyphs in 2px-stroke line style, brand palette (road, excavator, bridge, drainage pipe, tender/document, compass/survey, hard hat, crane). One sheet, sliced + remove_background.
- Logo / monogram: a "GE" construction monogram mark (chevron/road-marking geometry) for nav + favicon. User has no logo.
- OG image: 1200×630 wide social card in brand language.
- Head kit: favicon.ico + svg, apple-touch, 192/512 + maskable, site.webmanifest, theme-color.
- Video loop (cinema carrier): hero film scrub — seedance clip from hero still, slow push-in/rack-focus, → ~100 frames → canvas scrub. (B3 is the Tier-1; the scrub is the cinema carrier that complements it on the hero band.)

## Anti-convergence (first build in chat — enemy = model's statistical default)
1. Palette: blue-black + bone + road-sign yellow (not graphite+amber, not neon-on-black).
2. Type: Satoshi + JetBrains Mono (not Inter).
3. Hero architecture: full-bleed 3D image-first / asymmetric (not centered, not left-text/right-image).
4. Tier-1: B3 3D subject scene orbit (not passive autoplay loop).
5. CTA garments: viewfinder crosshair + route-arrow link + shear row + stamp submit (rationed garments: ≤1 of the common trio).
6. Corner language: sharp hairline blueprint (no soft rounded, no pill).
All six derived from the brief's material world (asphalt, concrete, blueprint, signage).
