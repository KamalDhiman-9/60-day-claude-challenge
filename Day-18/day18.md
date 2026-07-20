# Day 18 — Custom Claude Skill: Brain Dump → Action Plan Dashboard

## Overview
Today I built and tested a custom Claude skill (`brain-dump-action-planner`) that converts messy, unstructured input — meeting transcripts, voice memo notes, brainstorming dumps — into a structured, interactive HTML dashboard covering summaries, action items, decisions, risks, conflicts, and open questions.

## What the Skill Does
- Parses raw/unstructured text (e.g. a meeting transcript PDF)
- Extracts and organizes it into fixed sections:
  - Summary
  - Key Takeaways
  - Action Items (Task / Owner / Deadline / Status table)
  - Open Questions
  - Risks / Blockers
  - Conflicts
  - Additional Notes
  - (Transcript Mode) Speaker Summary, Decisions by Speaker, Action Items by Speaker
- Renders everything as a self-contained, mobile-responsive HTML dashboard (Notion/Linear/Asana-style) with status badges (🔴🟠🟢⚠️❓✅⏳)
- Strict rule: never invents, infers, or assumes missing information — uses "Not specified" instead

## Test Input
Used a sample "Quarterly Growth Strategy Meeting" transcript (multi-speaker: CEO, Head of Sales, CFO, VP Marketing, Product Director, CTO, Customer Success Lead) covering:
- Q2 revenue shortfall (12% actual vs. 18% target)
- Enterprise deal slippage due to procurement delays
- Website redesign vs. engineering capacity conflict
- Rising support tickets tied to reporting/dashboard performance
- Postponed hiring and conference budget decisions

## Generated Dashboard — Structured Outputs
The skill produced:
- **8 action items** with owner/status where known, and "Not specified" where deadlines weren't given in the transcript
- **5 open questions** (e.g. will slipped deals close before year-end targets are missed)
- **5 risks/blockers** (e.g. engineering capacity constraints, incomplete architecture review)
- **2 explicit conflicts** flagged (redesign vs. engineering bandwidth; mismatched hiring headcount requests)
- **Per-speaker breakdown**: summary, decisions, and action items attributed to each of the 7 speakers, with attribution notes where ownership was ambiguous (e.g. "leadership team" as a general owner rather than one person)

*(Screenshot of the rendered dashboard to be added here.)*

`![Dashboard Screenshot](./screenshot.png)`

## Key Learnings
1. **Constraining the model to "never invent missing data"** produced a much more trustworthy output — every gap was explicitly marked "Not specified" instead of being silently filled in, which matters a lot for real meeting notes where inaccuracy is costly.
2. **Structuring the skill file as strict output rules + required sections** (rather than a loose prompt) made outputs consistent across different input types (transcripts vs. plain brain dumps vs. merged notes).
3. **Transcript Mode required extra care**: attributing action items and decisions per speaker only when the transcript actually assigned ownership, and explicitly flagging cases where the owner was implied but not stated (e.g., "everyone" vs. a named person).
4. **Rendering as an interactive HTML artifact** (cards, tables, badges, collapsible speaker sections) made the output dramatically more usable than a flat markdown or bullet-point summary — closer to a real project management dashboard than a text summary.
5. **Separating sections rigidly** (Risks vs. Conflicts vs. Open Questions) forced clearer thinking about *why* something is unresolved — is it a blocker, a disagreement, or just an unanswered question — which a single "notes" dump tends to blur together.

## Files
- `day18.md` — this file
- `screenshot.png` — dashboard screenshot (to be added)
