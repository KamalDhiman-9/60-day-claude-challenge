# 🔍 AI Job Red Flag Detector

**60 Days of Claude Challenge — Day 14/60**

A prompt-engineered tool that analyzes job descriptions and company information to flag red flags *before* you apply — mismatched seniority requirements, hustle-culture language, hidden relocation clauses, and hiring risks — so you can make an informed decision instead of finding out three weeks in.

---

## 💡 Why I Built This

Job hunting means reading dozens of postings that sound great on the surface but hide warning signs in plain language: "fast-paced," "work hard play hard," "like a family," 5+ years required for a "Junior" role. This tool turns that pattern-recognition into a repeatable, structured process.

## ⚙️ What It Does

- **Unrealistic Requirements** — flags experience/title mismatches, stacked tech stacks, contradictory expectations
- **Toxic Workplace Signals** — detects burnout indicators, "wear many hats," hustle-culture phrasing
- **Remote Job Authenticity** — surfaces hidden office/relocation requirements behind "remote" claims
- **Hiring Risks** — missing salary info, vague responsibilities, suspicious hiring speed
- **Company Risk** — funding, team size, stability, and reputation signals
- **Output** — a weighted risk score (0–100), severity-ranked red flag table, category risk breakdown, a clear verdict (✅ / ⚠️ / ❌), and 5 tailored interview questions to validate the flags directly with the recruiter

## 🧪 Test Run

Fed it a sample "Junior Full Stack Developer" posting requiring 5+ years experience, 7 languages/frameworks, 3 cloud platforms, and 24/7 support — with no salary listed and a hidden relocation clause.

**Result:** `88/100` risk score → **❌ Avoid**

## 📋 The Prompt

```
You are an AI Red Flag Detector for job seekers.
Analyze the Job Description and Company Information.

Identify:
1. Unrealistic Requirements
   - Excessive experience for the role
   - Too many skills/responsibilities
   - Contradictory expectations
2. Toxic Workplace Signals
   - Burnout indicators
   - 'Wear many hats'
   - 'Fast-paced', 'rockstar', 'hustle culture'
   - Poor work-life balance signals
3. Remote Job Authenticity
   - Hidden office requirements
   - Relocation expectations
   - Misleading remote claims
4. Hiring Risks
   - Missing salary information
   - Vague responsibilities
   - Excessive qualifications
   - Suspicious hiring practices
5. Company Risks
   - Reputation concerns
   - Stability concerns
   - Growth or layoff indicators

Output:
## Overall Risk Score (0-100)
### Top Red Flags
- List with severity (1-10)
### Positive Signals
- List positives
### Risk Breakdown
| Category | Risk Level |
|-----------|-----------|
| Requirements | |
| Culture | |
| Remote | |
| Hiring | |
| Company | |
### Final Verdict
✅ Apply
⚠️ Apply with Caution
❌ Avoid
### 5 Smart Interview Questions
Generate questions that help validate the identified risks.

Job Description:
[Paste Here]

Company Information:
[Paste Here]
```

## 🎯 Key Takeaway

Structured prompt design — weighted scoring, categorized breakdowns, tabular output — turns an LLM from a generic chatbot into a genuine decision-support tool. Constraining the output format is what makes the difference between "vague advice" and "actionable analysis."

## 🛠️ Possible Next Steps

- [ ] Turn this into a small web app (paste JD → get report)
- [ ] Add scraping support for LinkedIn/Indeed postings
- [ ] Batch mode — compare risk scores across multiple postings
- [ ] Weight the risk score algorithmically instead of purely via prompt

---

`#60DaysOfClaude` `#ABTalks` `#AI` `#PromptEngineering` `#JobSearch` `#BuildInPublic`
