# Day 16/60 — Building a Stock Fundamental Research Skill for Claude 📊

**#60DaysClaudeChallenge**

Today I built and tested a custom **Claude Skill** for fundamental analysis of Indian and global listed stocks — and ran it end-to-end on **HDFC Bank (NSE: HDFCBANK)** as a live case study.

## What I built

A skill spec (`stock-fundamental-research`) that turns Claude into a disciplined equity research assistant with hard guardrails:

- **No buy/sell/hold calls, no target prices, no personalized investment advice** — ever. The skill is designed to inform, not to recommend.
- **Live-data-first sourcing** with cross-checking across Screener, Tickertape, Moneycontrol, NSE/BSE, annual reports, and earnings calls.
- **No fabrication rule** — if a figure can't be verified, the skill forces a `🚩 Data unavailable — verify at [source]` flag instead of guessing.
- **Five output modes**: Quick Take, Deep Dive, Compare, Pros & Cons, and Portfolio Fit — each with a defined structure and word/format budget.
- A standardized **interpretation rulebook** for valuation, D/E, interest coverage, current ratio, FCF quality, and ROE/ROCE bands, so every stock gets judged against the same yardstick.

## Test run: HDFC Bank Deep Dive

Ran the skill in Deep Dive mode on HDFC Bank. Some things that stood out from the output:

- **Valuation**: P/E ~16.9x, P/B ~2.1x — trading at a discount to its own history and to ICICI Bank, largely due to post-merger normalization.
- **Growth**: 5Y profit CAGR of 19%, but TTM growth has slowed to 8% — the merger with HDFC Ltd (July 2023) makes YoY comparisons noisy, and the skill correctly flagged this rather than treating it as a red flag.
- **Asset quality**: GNPA at 1.15%, among the best in the sector.
- **Ownership**: HDFC Bank has had **0% promoter holding** since the merger — a structural quirk (HDFC Ltd itself had no single promoter) that a naive analysis could easily misread as a governance concern.
- **Governance flag**: CEO reappointment still pending NRC/RBI process — the kind of detail that's easy to miss if you're only looking at ratios.
- The skill also correctly caveated that traditional **D/E and current-ratio rules don't map cleanly onto bank balance sheets**, instead of blindly applying the generic interpretation rubric.

## What I learned

1. **Guardrails are a feature, not friction.** Forcing "no fabrication" and "no recommendation" rules actually produced a *more* useful report — it pushed toward verifiable facts and flagged data conflicts instead of smoothing them over.
2. **Domain-specific interpretation rules matter.** A generic "high D/E = risky" heuristic breaks completely for banks. Good skill design means encoding where the rules of thumb don't apply.
3. **Cross-source verification catches real errors.** One aggregator reported an obviously wrong P/B ratio (365x) — cross-checking against Screener's book value caught and excluded it instead of it silently propagating into the report.

## Next up

Testing the **Compare** and **Portfolio Fit** modes next — curious how the skill handles multi-stock sector overlap analysis.

---
*Part of my #60DaysClaudeChallenge with ABTalks — building practical, guardrailed AI workflows one day at a time.*

**Disclaimer:** This post documents an educational AI-assisted research workflow. Nothing here is investment advice.
