# Project Context: SCTP DSAI Technical Entry Assessment v2

**Last updated:** 2026-06-22  
**Repo:** [github.com/cpwong/5m-data-entry-test-v2](https://github.com/cpwong/5m-data-entry-test-v2)  
**Local draft folder:** `C:\dev\sctp-dsai\5m-data-entry-test-draft\`  
**Original repo (do not modify):** [github.com/su-ntu-ctp/5m-data-entry-test](https://github.com/su-ntu-ctp/5m-data-entry-test)

---

## What This Is

A full revision of the technical entry assessment for the **(SCTP) Advanced Professional Certificate in Data Science and AI** programme. The original assessment (Q1–Q7 only, all `.py`) was replaced with a 10-question set covering five topic areas, in a mix of `.md` (MCQ/short answer) and `.py` (code/commands) formats.

---

## Repository Structure

```
5m-data-entry-test-draft/
├── README.md                  # Main assessment document (learner-facing)
├── CONTEXT.md                 # This file
├── src/
│   ├── q1.md                  # Python: Variables and Constants (MCQ)
│   ├── q2.md                  # Python: Packages, Environments, Conda (MCQ + stretch)
│   ├── q3.md                  # CLI: Basic Navigation (MCQ)
│   ├── q4.md                  # GitHub: Core Concepts (MCQ)
│   ├── q5.md                  # OS Concepts (MCQ)
│   ├── q6.md                  # OS: WSL and Terminal Shells (short answer)
│   ├── q7.md                  # AI Literacy: Prompt Engineering (short answer)
│   ├── q8.py                  # Python: Loops and Functions (code)
│   ├── q9.py                  # CLI: Directory Navigation and File Creation (commands)
│   └── q10.py                 # GitHub: Git Workflow (commands)
└── answers/
    └── answer-key.md          # Assessor-only model answers + rubric
```

---

## Assessment Design

### Topic Coverage

| Area | Questions | Format |
|------|-----------|--------|
| Python Programming | Q1, Q2, Q8 | MCQ + short answer / code |
| Command Line Interface (CLI) | Q3, Q9 | MCQ + commands |
| Git and GitHub | Q4, Q10 | MCQ + commands |
| Operating Systems | Q5, Q6 | MCQ + short answer |
| AI Literacy | Q7 | Short answer |

### Scoring

| Question | Topic | Marks |
|----------|-------|-------|
| Q1 | Python: Variables & Constants | 3 |
| Q2 | Python: Packages & Conda | 3 + 2 bonus |
| Q3 | CLI: Navigation | 4 |
| Q4 | GitHub: Core Concepts | 4 |
| Q5 | OS Concepts | 4 |
| Q6 | OS: WSL & Terminals | 6 |
| Q7 | AI Literacy | 6 |
| Q8 | Python: Loops & Functions | 4 |
| Q9 | CLI: Commands | 6 |
| Q10 | GitHub: Git Workflow | 6 |
| **Total** | | **46 (+2 bonus)** |

**Pass threshold (recommended):** 28/46 (60%)

---

## Key Design Decisions

- **`.md` for Q1–Q7** (non-coding): renders natively on GitHub; learners can fill in answers without an IDE.
- **`.py` for Q8–Q10** (coding/commands): requires a code editor; comments serve as answer slots.
- **Q2(d) is a stretch question** (⭐ bonus, 2 marks): tests `from dotenv import load_dotenv` + `import utils`.
- **OS-agnostic framing**: Q3 specifies Linux/macOS/WSL context; Q9 includes `touch` (Linux/macOS/WSL) and `New-Item` (PowerShell) hints.
- **Q6(c) is conceptual** (terminal emulator vs shell, with examples) — deliberately avoids duplicating Q9's CLI commands task.
- **Q7** uses the original repo's `q8.py` prompt engineering question (Prompt A vs Prompt B comparison).
- **Q10** references `q8.py` (not `q1.py`) in the scenario — corrected from original.
- **No timing constraints** anywhere in the assessment.
- **No Expected Audience section** in README.
- **No em/en dashes in prose** (replaced with commas, colons, or restructured sentences; dashes kept only in hyperlink label text reflecting actual page titles).

---

## README Structure

1. **About This Assessment** — purpose, what we expect, what this is not
2. **What This Assessment Covers** — topic/question/format table
3. **Submission Instructions** — fork → clone → complete → push → submit link
   - Framed as part of the assessment itself (self-directed learning signal)
   - Troubleshooting table
   - Self-learning callout blockquote
4. **References** — grouped by topic area, no timing estimates
5. **Problems** — 10 question links pointing to `./src/`
6. **Use of Generative AI Tools** — expanded policy with industry-standard framing

---

## Submission Workflow (for Learners)

1. Fork `cpwong/5m-data-entry-test-v2` on GitHub
2. Clone their fork locally
3. Complete `src/q1.md` through `src/q10.py`
4. `git add . && git commit -m "Complete entry assessment" && git push origin main`
5. Submit forked repo URL via NTU Survey Portal

---

## Links Verified (2026-06-22)

All links in README.md were checked. Two fixes applied:

| Issue | Fix |
|-------|-----|
| GeeksForGeeks URL 404 (`/difference-between-terminal-shell-console-and-command-line/`) | Replaced with `https://www.geeksforgeeks.org/operating-systems/what-is-terminal-console-shell-and-kernel/` |
| Git Handbook (guides.github.com) redirects to GitHub Docs | Updated URL and label to `https://docs.github.com/en/get-started/using-git/about-git` |

All other links confirmed live: GitHub Docs (4 links), W3Schools Git, 3 YouTube videos, freeCodeCamp, conda docs, PyPI python-dotenv, Microsoft Docs WSL (2 links), LearnPrompting.org, OpenAI prompt guide, W3Schools Python (5 pages).

---

## Git History

| Commit | Description |
|--------|-------------|
| Initial commit | All files pushed to repo root |
| Move question files into src/ folder | Renamed q1–q10 into `src/` subdirectory |

> Note: The `src/` move was staged via bash (`git add -A`) in the sandbox session but requires a terminal commit and push from the user's machine:
> ```bash
> cd C:\dev\sctp-dsai\5m-data-entry-test-draft
> git commit -m "Move question files into src/ folder"
> git push origin main
> ```

---

## Pending / Next Steps

- [ ] Confirm `git commit` and `git push` for the `src/` restructure completed successfully
- [ ] Share repo link with NTU / programme team for review
- [ ] Update NTU Survey Portal with the correct repo URL for applicants to fork
