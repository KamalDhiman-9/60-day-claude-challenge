# Day 15/60 — Building a Vedic Astrology Assistant Prompt with Claude

### 🎯 Goal
Design a structured prompt that turns Claude into a domain-specific "expert" persona — a Vedic astrologer covering Parashara, Jaimini, Nakshatra, Vimshottari Dasha, and Transit analysis — and test how well an LLM handles a knowledge domain that depends on precise mathematical calculations rather than pure language reasoning.

### 🛠️ What I Built
A multi-section system prompt that:
- Collects structured user inputs (birth details, concerns, etc.) before generating output
- Enforces a fixed output schema: Birth Chart Summary → Life Pattern Analysis → Career/Wealth → Relationships → Dasha Analysis → 5-Year Forecast → Remedies
- Uses markdown tables for forecasts to keep output scannable
- Includes explicit output rules (separate facts vs. interpretation, prioritize practical guidance)

### 🔍 Key Learning
The most interesting result wasn't the astrology output — it was watching Claude **flag its own limitation** before generating anything. Vedic astrology depends on:
- Sidereal (not tropical) zodiac calculations
- Correct ayanamsha values
- Precise ephemeris data for planetary degrees
- Exact birth time → house cusps → Lagna

Without a calculation engine (no astronomy API/tool wired in), Claude correctly refused to fabricate a "confident-sounding" chart with invented planetary positions. It offered a partial, verifiable fact (sidereal Sun sign, since that's date-based and doesn't need birth time) and asked the user to bring back precise chart data from a proper ephemeris tool before doing interpretation work.

### 💡 Takeaway for Prompt Engineering
> **A well-designed expert-persona prompt isn't just about output format — it should also define what the model does when it lacks the tools to be accurate.**

This is a good template pattern for any "expert domain" prompt where the domain relies on external computation (astrology, financial modeling, engineering calcs, etc.):
- Build the persona and output schema clearly
- Plan for the "I don't have a calculator/API for this" case
- Decide whether the model should refuse, caveat, or hand off to a tool

### 🔗 Next Steps
- Wire up an actual ephemeris/astronomy API (e.g., Swiss Ephemeris) as a tool so Claude can compute real placements
- Test the same prompt pattern with Claude Code + a Python astrology library
- Compare interpretation quality once real chart data is fed in vs. this "no-tool" fallback behavior

---

*Part of my #60DaysOfClaude challenge — exploring prompt engineering, agentic tooling, and LLM behavior one day at a time.*
