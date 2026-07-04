# 30-Day Prompt Engineering & Claude AI Mastery Roadmap

**Goal:** Go from prompt-engineering beginner to someone who can design, evaluate, and ship Claude-powered workflows — with a portfolio project and public content to show for it.

**Format:** ~1 hour/day. Each week ends in a mini-project you can turn into an ABTalks post or GitHub artifact.

---

## Week 1 (Days 1–7): Foundations — How LLMs "Think" & Basic Prompting

**Milestone:** Understand how Claude processes prompts, and reliably write clear zero-shot and few-shot prompts.

| Day | Task | Resource |
|---|---|---|
| 1 | Read how LLMs predict tokens; understand context windows, temperature | Anthropic's "Prompt engineering overview" (docs.claude.com) |
| 2 | Write 5 zero-shot prompts for different tasks (summarize, classify, extract, rewrite, explain) | Claude.ai or API playground |
| 3 | Learn "be clear and direct" principle — rewrite 3 vague prompts into precise ones | docs.claude.com/prompt-engineering |
| 4 | Few-shot prompting: give Claude 2–3 examples before the real task; compare output vs zero-shot | Test in Claude.ai |
| 5 | Learn about system prompts vs user prompts; write 3 system prompts for different "personas" | Anthropic docs — system prompts |
| 6 | Practice output formatting requests (bullet lists, tables, JSON) | Self-practice |
| 7 | **Mini-project:** Build a "prompt style comparison" doc — same task, 3 prompt styles, side-by-side outputs | — |

**Week 1 Resources:** docs.claude.com/en/docs/build-with-claude/prompt-engineering, Anthropic Prompt Library

---

## Week 2 (Days 8–14): Core Techniques — Structure, Reasoning, Roles

**Milestone:** Use XML tags, chain-of-thought, and role-based prompting to control Claude's reasoning and output reliably.

| Day | Task | Resource |
|---|---|---|
| 8 | Learn XML tag structuring (`<task>`, `<context>`, `<example>`) for complex prompts | Anthropic docs — use XML tags |
| 9 | Chain-of-thought: ask Claude to "think step-by-step" before answering; compare accuracy on a reasoning task | Test with a logic/math problem |
| 10 | Role-based prompting: assign Claude expert personas (e.g. "You are a senior data analyst") | Practice on 3 different roles |
| 11 | Prefilling & response formatting — control exact output structure (JSON schema, headers) | docs.claude.com |
| 12 | Negative examples — show Claude what NOT to do alongside what to do | Self-practice |
| 13 | Multi-turn prompting — build a 4–5 turn conversation that refines an output iteratively | Claude.ai |
| 14 | **Mini-project:** Design a "prompt template" for one real use case (e.g. resume feedback bot) using system prompt + XML tags + examples | — |

---

## Week 3 (Days 15–21): Advanced Patterns — Tool Use, Agents, Evaluation

**Milestone:** Understand tool use/function calling, basic RAG concepts, and how to evaluate prompt quality systematically.

| Day | Task | Resource |
|---|---|---|
| 15 | Learn tool use / function calling conceptually — how Claude decides to call a tool | Anthropic docs — tool use |
| 16 | Build a simple tool-use example via API (e.g. a weather or calculator tool) | Claude API + Python |
| 17 | Learn RAG basics — why retrieval matters, chunking, embeddings (conceptual, not deep math) | Anthropic docs / intro articles |
| 18 | Try a mini RAG-lite: paste a document into context and design prompts that ground answers in it | Claude.ai with long context |
| 19 | Prompt evaluation — learn how to define success criteria and test prompts against edge cases | Self-practice: write 5 edge-case tests for one prompt |
| 20 | Iterative refinement — take Day 14's prompt template and stress-test + improve it | — |
| 21 | **Mini-project:** Build a small Python script using Claude API with one tool call and structured JSON output | Claude API docs |

---

## Week 4 (Days 22–30): Applied Capstone — Build, Ship, Publish

**Milestone:** Ship one complete, working Claude-powered mini-project and publish your learning publicly.

| Day | Task | Resource |
|---|---|---|
| 22 | Pick a capstone idea (e.g. AI study-buddy, LinkedIn post generator, resume analyzer) | Your choice — public-welfare angle if possible |
| 23 | Design the prompt architecture: system prompt + XML structure + examples + expected output format | — |
| 24 | Build core logic in Python using the Claude API | api.anthropic.com docs |
| 25 | Add error handling + test with 5–10 varied inputs | — |
| 26 | Polish output formatting and add a simple interface (CLI or basic script) | — |
| 27 | Write a README documenting your prompt design decisions (why you structured it this way) | GitHub |
| 28 | Push project to GitHub with clear commit history | GitHub |
| 29 | Turn the project + key lessons into an ABTalks LinkedIn post (before/after prompt examples work great here) | Your existing ABTalks format |
| 30 | **Capstone Review:** Reflect on what changed in how you write prompts since Day 1; list 3 techniques you'll use in every future prompt | — |

---

## Final Outcome (Day 30)

By the end of 30 days, you'll have:
- A working **Claude-powered mini-project** on GitHub with documented prompt design choices
- A personal **prompt template library** (from Weeks 1–2 mini-projects) you can reuse
- One **published LinkedIn post** (ABTalks-style) showcasing the project and what you learned
- A concrete answer to "I understand prompt engineering" backed by evidence, not just claims — directly closing part of your visibility gap

**Natural next step:** Feed this project into your 6-month AI Engineer roadmap as the "LLMs/APIs" phase deliverable, and move into RAG/agents next.
