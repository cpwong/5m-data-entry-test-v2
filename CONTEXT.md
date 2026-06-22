# Project Context: SCTP DSAI Technical Entry Assessment v2

**Last updated:** 2026-06-22  
**Dev repo (this working copy):** [github.com/cpwong/5m-data-entry-test-v2](https://github.com/cpwong/5m-data-entry-test-v2)  
**Local path:** `/home/cpwong/sctp-dsai/5m-data-entry-test-v2`  
**Public applicant-facing repo (fork target):** [github.com/su-ntu-ctp/5m-data-entry-test](https://github.com/su-ntu-ctp/5m-data-entry-test) — the NTU Survey Portal points applicants here. The v2 content in this dev repo will eventually be published to that repo so the public URL stays stable across assessment versions.

---

## What This Is

A revision of the technical entry assessment for the **(SCTP) Advanced Professional Certificate in Data Science and AI** programme. The current iteration is a 9-question set covering five topic areas, in a mix of `.md` (MCQ, paste-real-output, short answer) and `.py` (read / fix / write code and commands) formats.

This version was further restructured after an initial 10-question layout: Q1 was consolidated into a 15-part mixed MCQ block, the stretch dotenv question was retired, and a "read and predict output" question (Q7) and a "find and fix the bug" question (Q8) were added in place of the older loops-and-functions write-from-scratch task.

---

## Repository Structure

```
5m-data-entry-test-v2/
├── README.md                  # Main assessment document (learner-facing)
├── CLAUDE.md                  # Repo guidance for Claude Code
├── CONTEXT.md                 # This file
├── src/
│   ├── q1.md                  # Mixed MCQ (15 parts): Python, CLI, Git, OS, shells
│   ├── q2.md                  # Python & Environment Setup (paste real terminal output)
│   ├── q3.md                  # OS / Shell / WSL (paste real output + short answers)
│   ├── q4.md                  # CLI: Navigation and Predicting Output (commands + predict)
│   ├── q5.md                  # OS: WSL, Terminals, Shells (short answer, 3 parts)
│   ├── q6.md                  # AI Literacy: Prompt Engineering (A vs B + rewrite)
│   ├── q7.py                  # Python: Read and Predict Output
│   ├── q8.py                  # Python: Find and Fix the Bug
│   └── q9.py                  # GitHub: Git Workflow (5 commands + short answer)
├── answers/
│   └── answer-key.md          # Assessor-only model answers + rubric
└── .proposed-feng/            # Parallel WIP draft from Feng (do not cross-apply to src/)
```

---

## Assessment Design

### Topic Coverage

| Area | Questions |
|------|-----------|
| Python Programming | Q1 (parts), Q2, Q7, Q8 |
| Command Line Interface (CLI) | Q1 (parts), Q4 |
| Git and GitHub | Q1 (parts), Q9 |
| Operating Systems / Shells | Q1 (parts), Q3, Q5 |
| AI Literacy | Q6 |

Q1 spans all five topic areas in a single mixed MCQ block.

### Scoring (proposed; programme team to confirm before next cohort)

| Question | Topic | Marks |
|----------|-------|-------|
| Q1 | Mixed MCQ (15 parts × 1) | 15 |
| Q2 | Python & Environment Setup | 10 |
| Q3 | OS / Shell / WSL | 10 |
| Q4 | CLI: Navigation + Predict | 10 |
| Q5 | OS short answers | 10 |
| Q6 | AI Literacy + rewrite | 15 |
| Q7 | Read and Predict Output | 10 |
| Q8 | Find and Fix the Bug | 10 |
| Q9 | Git Workflow | 10 |
| **Total** | | **100** |

**Pass threshold (recommended):** 60/100 (60%).

**Optional hard gate (recommended):** require ≥ 6/10 on Q2 so a learner cannot pass purely on MCQ recognition without a working environment or an honest, specific account of what is missing. MCQ alone caps at 15/100; the gate enforces that the recognition route cannot suffice on its own.

---

## Key Design Decisions

- **`.md` for Q1 to Q6** (non-coding or paste-output): renders natively on GitHub; learners can fill in answers without an IDE.
- **`.py` for Q7 to Q9** (coding / commands): requires a code editor; comments serve as answer slots.
- **Q1 is a 15-part mixed MCQ** consolidating the previously separate Python-constants, conda, CLI, Git, and OS MCQ blocks. Trades narrow coverage per question for breadth.
- **Q2 and Q3 require pasting real terminal output** from the learner's own machine. Signals follow-through and honesty over recognition. Honesty-about-not-installed answers are explicitly accepted.
- **Q7 (read code) and Q8 (fix code) are split** to separate two distinct skills: reasoning about code by reading it, and diagnosing a wrong result.
- **Three-class platform framing (macOS / Linux / Windows-WSL)**: macOS, Linux, and WSL are treated as equal POSIX paths; PowerShell is the outlier the assessment warns against. Q2 uses an explicit 3-row platform table so every candidate sees their own row. Q3 title is platform-neutral ("Your Operating System and Shell"); Q3(c) asks a general-knowledge question about why PowerShell breaks POSIX course instructions, answerable without first-hand PowerShell experience. Q5(b) keeps the WSL-specific misconception because it is the most common Windows-onboarding failure; the underlying skill (critiquing an OS misconception) is OS-agnostic. README references section groups links under General / macOS / Linux / Windows-WSL headings.
- **AI literacy** uses the Prompt A vs Prompt B comparison plus a rewrite task. The rewrite is the discriminating part: borrowing one element forces the learner to articulate why.
- **No timing constraints** anywhere in the assessment.
- **No em/en dashes in prose** (replaced with commas, colons, or restructured sentences; dashes kept only in question/section headings and step labels that match README link text).

---

## README Structure

1. **About This Assessment** — purpose, what we expect, what this is not
2. **What This Assessment Covers** — topic/question/format table
3. **Submission Instructions** — fork → clone → complete → push → submit link
   - Framed as part of the assessment itself (self-directed learning signal)
   - Troubleshooting table
   - Self-learning callout blockquote
4. **References** — grouped by topic area, no timing estimates
5. **Problems** — 9 question links pointing to `./src/`
6. **Use of Generative AI Tools** — expanded policy with industry-standard framing

---

## Submission Workflow (for Learners)

1. Fork `cpwong/5m-data-entry-test-v2` on GitHub
2. Clone their fork locally
3. Complete `src/q1.md` through `src/q9.py`
4. `git add . && git commit -m "Complete entry assessment" && git push origin main`
5. Submit forked repo URL via NTU Survey Portal

---

## Links Verified (2026-06-22)

All links in README.md were checked on the initial publication. Two fixes were applied at that time:

| Issue | Fix |
|-------|-----|
| GeeksForGeeks URL 404 (`/difference-between-terminal-shell-console-and-command-line/`) | Replaced with `https://www.geeksforgeeks.org/operating-systems/what-is-terminal-console-shell-and-kernel/` |
| Git Handbook (guides.github.com) redirects to GitHub Docs | Updated URL and label to `https://docs.github.com/en/get-started/using-git/about-git` |

All other links confirmed live: GitHub Docs, W3Schools Git, YouTube videos, freeCodeCamp, conda docs, PyPI python-dotenv, Microsoft Docs WSL, LearnPrompting.org, OpenAI prompt guide, W3Schools Python.

Re-verify links before next cohort.

---

## Pending / Next Steps

- [ ] Programme team to confirm or adjust the proposed 100-mark scoring split, and decide whether to enforce the Q2 hard gate.
- [ ] Re-verify all README hyperlinks before publishing to applicants.
- [ ] Share dev repo link with NTU / programme team for review.
- [ ] Publish approved v2 content to `su-ntu-ctp/5m-data-entry-test` (the public fork target). NTU Survey Portal URL does not change.
