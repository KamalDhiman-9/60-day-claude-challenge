# Day 21 — Digital Footprint & Privacy Dashboard

## What I built
An interactive, single-file HTML dashboard that estimates a person's "digital footprint"
and privacy exposure from a self-reported list of 15 apps (Instagram, Snapchat, TikTok,
YouTube, Discord, WhatsApp, iMessage, Spotify, Roblox, PUBG Mobile, Amazon, Meesho,
Google Search, Google Pay, Google Photos).

Styled as a premium cybersecurity/SaaS dashboard (Notion/Stripe/Apple Privacy Report
inspired), dark theme, cyan/violet accents.

## Sections implemented
1. **Digital Footprint Score** — 72/100 (🟠 Significant)
2. **Privacy Score** — 38/100 (🟠 Fair)
3. **Exposure Heatmap** — per-app exposure level, color-coded
4. **Company Exposure Ranking** — parent companies ranked by service count
   (Alphabet/Google leads with 4 of 15 services)
5. **Data Collection Matrix** — location/contacts/financial/behavioral/media
   likelihood per app
6. **Risk Radar** — SVG hexagonal radar chart across 6 risk axes
7. **Digital Twin Profile** — composite behavioral estimate (age bracket,
   region signal, content habits, shopping style)
8. **Most Valuable Data Assets** — ranked list of the highest-value data
   categories being generated (watch-time, search intent, social graph, etc.)
9. **Privacy Improvement Plan** — prioritized, actionable recommendations
   (High/Medium/Low impact)
10. **Final Verdict** — footprint vs. privacy score summary

## Key design constraint: Facts vs. Estimates
The hardest part of this build wasn't the UI — it was the epistemics. The brief
required strictly separating:
- **Facts**: the 15 services themselves + their publicly known parent companies
- **Estimates**: literally everything derived from those facts — scores, rankings,
  heatmap levels, the entire Digital Twin Profile, and all improvement advice

Every section is explicitly tagged (FACT / ESTIMATE badges), the report never
claims certainty about inferred traits, and it never implies access to any real
private database. Where a trait couldn't reasonably be inferred (e.g. mobility/
travel signal), it explicitly returns "Not enough information provided" instead
of guessing.

## Findings / privacy takeaways
- Google/Alphabet is the single largest point of concentration — 4 of the 15
  services (Search, YouTube, Pay, Photos) all route through one company, meaning
  a single account compromise or policy change has outsized reach.
- Social + short-form video apps (Instagram, TikTok, Snapchat) score highest on
  the exposure heatmap due to continuous behavioral + location + social-graph
  data collection.
- The most "valuable" data assets aren't financial — behavioral/watch-time data
  and search intent history rank above purchase history for targeting value.
- Encrypted/closed-ecosystem apps (iMessage, Spotify) consistently score lowest
  on exposure, reinforcing that platform *design*, not just usage frequency,
  drives real exposure.

## What I'd improve next time
- Turn the Privacy Improvement Plan into an actual interactive simulator —
  let toggling an app on/off live-update the Digital Footprint Score, rather
  than a static recommendation list.
- Add a second radar overlay showing "score if recommendations are applied"
  vs. "current state" for a clearer before/after.

## Files
- `dashboard.html` — full interactive dashboard artifact
- `screenshots/` — captures of each dashboard section

## Tech
Single-file HTML/CSS (no framework), inline SVG for the radar chart, CSS custom
properties for theming, responsive grid layout.
