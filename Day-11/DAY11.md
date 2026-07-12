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
Project Role : AI / ML Engineer
Project Role Description : Develops applications and systems that utilize AI tools, Cloud AI services, with proper cloud or on-prem application pipeline with production ready quality. Be able to apply GenAI models as part of the solution. Could also include but not limited to deep learning, neural networks, chatbots, image processing.
Must have skills : Machine Learning (ML)
Good to have skills : NA
Minimum 2 year(s) of experience is required
Educational Qualification : 15 years full time education

Summary:
These roles have many overlapping skills with GENAI Engineers and architects. Description may scaleup/scale down based on expected seniority.
# ATS Resume Optimizer & Resume Generator
Input:
* Existing Resume
* Target Job Description
Task:
Rewrite the resume for maximum ATS alignment and recruiter relevance while maintaining 100% factual accuracy.
Rules:
* Never invent experience, projects, employers, certifications, dates, metrics, or skills.
* Only optimize, reorganize, and rephrase existing content.
* Use relevant JD keywords naturally.
* Keep ATS-friendly formatting.
Output:
1. ATS Match Score
2. Gap Analysis
   * Missing Keywords
   * Missing Skills
   * Improvement Opportunities
3. Updated Resume
Return the complete rewritten resume as a professional resume document using the following structure:
# FULL NAME
Phone | Email | LinkedIn | GitHub
## PROFESSIONAL SUMMARY
## SKILLS
## EXPERIENCE
## PROJECTS
## EDUCATION
## CERTIFICATIONS
## ACHIEVEMENTS
The resume should be fully formatted, ready to copy into Word, Google Docs, FlowCV, Overleaf, or Canva without additional editing.

---

`#AI #Claude #ResumeBuilder #ATS #60DaysOfCode #BuildInPublic`
