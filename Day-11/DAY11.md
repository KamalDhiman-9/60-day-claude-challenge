# 🚀 Day 11/60 — #60DaysClaudeChallenge by @abtalks

## 🎯 Project: ATS Resume Optimizer & Resume Generator

Today I built a tool that takes an existing resume + a target job description and rewrites the resume for maximum **ATS alignment** — without inventing a single fact.

### How it works
- 📄 Input: Resume (PDF) + Job Description
- 🔍 Analyzes keyword overlap between resume and JD
- 📊 Generates an **ATS Match Score**
- 🕳️ Runs a **Gap Analysis** — missing keywords, missing skills, improvement opportunities
- ✍️ Outputs a fully reformatted, ATS-friendly resume — ready to paste into Word, Google Docs, or Canva

### Key rule I enforced
Zero hallucination. No fake experience, no invented metrics, no made-up skills — only reorganizing and rephrasing what's actually true, using the JD's language naturally.

### Real test
Ran it on my own resume against an AI/ML Engineer JD requiring 2+ years experience. The tool didn't just optimize keywords — it also flagged the honest gap (my experience is ~4 months of internships), which is exactly the kind of transparency I want from an AI resume tool, not empty score inflation.

**Stack:** Claude for structuring/generation, Python (docx) for formatted output generation.

### What's next
Turning this into a reusable prompt template / mini-workflow anyone can plug their resume + JD into.

---

`#AI #Claude #ResumeBuilder #ATS #60DaysOfCode #BuildInPublic`
