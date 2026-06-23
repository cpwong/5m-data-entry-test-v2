# Revised Entry Assessment (v3 draft) — Rationale

This is a **redesign** of the entry assessment, aimed at the real goal:

> Screen learners *without* a technical background for the **operational
> environment literacy** that AI-assisted coding does **not** paper over —
> can they actually use a terminal, understand their computer environment
> (WSL/shell/OS), and read basic Python?

## What changed and why

| Change | Why |
|--------|-----|
| **Added "paste your real terminal output" tasks** (Q1, Q2) | These cannot be answered by recognition or by pasting from ChatGPT — the output must come from the learner's own machine. This is the single highest-signal change and tests the thing that actually blocks beginners: *getting the environment to work.* |
| **Cut MCQ weight from ~60% to ~25%** | MCQs test recognition ("pick `mkdir`"), not capability ("create a folder"). A learner who has never opened a terminal can still guess by elimination. |
| **Python questions reframed to read / predict / fix** | AI trivially writes `count_evens`. It is harder to fake *understanding* code you must read and explain. This is also the skill that survives the AI era. |
| **Hardened distractors** on remaining MCQs | So guessing-by-elimination no longer earns a pass. |
| **Added a self-directed-learning reflection** (Q8c) | Directly probes the trait the programme says it is screening for. |
| **Kept the strongest originals**: WSL/terminal short answer, prompt-engineering, git workflow | These were already good, AI-resistant, and diagnostic. |

## Question map

| Q | Area | Format | What it really tests |
|---|------|--------|----------------------|
| Q1 | Environment | Paste real output | Python + conda actually installed and runnable |
| Q2 | OS / Shell / WSL | Paste real output + short answer | Knows what shell/OS they are on |
| Q3 | CLI | Commands + predict output | Can navigate and reason about a filesystem |
| Q4 | Python | Read & predict output | Reads code, not just writes it |
| Q5 | Python | Find & fix the bug | Understands what code does |
| Q6 | Git | Commands | Real version-control workflow |
| Q7 | OS / WSL | Short answer | Conceptual understanding in own words |
| Q8 | AI literacy | Short answer + reflection | Prompt sense + self-directed learning |

## Scoring philosophy

Marks are weighted so a learner **cannot pass on MCQs alone** — they must
produce real terminal output (Q1, Q2) and write in their own words (Q5, Q7, Q8).
The submission process itself (fork → clone → branch → commit → push) remains
part of the assessment and is the ultimate proof of competency.

## ⚠️ Note for assessors

Do **not** commit `answers/answer-key.md` to the repository that learners fork.
Keep it in a private assessor-only repo or release. (The current v2 repo ships
the key inside the forkable repo — fix this before reuse.)
