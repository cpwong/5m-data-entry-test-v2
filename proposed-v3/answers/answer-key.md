# Answer Key and Marking Rubric (v3 draft)

**For assessor use only — do NOT commit to the repo learners fork.**

---

## Scoring Summary

| Q | Topic | Format | Marks | AI-resistant? |
|---|-------|--------|-------|---------------|
| Q1 | Environment proof | Paste real output | 6 | ★ High — output must come from their machine |
| Q2 | OS / shell / WSL | Paste output + short answer | 5 | ★ High |
| Q3 | CLI navigation + predict | Commands + output | 6 | Medium |
| Q4 | Python read & predict | Short answer | 4 | Medium |
| Q5 | Python find & fix bug | Code | 4 | Medium |
| Q6 | Git workflow | Commands | 6 | Medium (submission proves it too) |
| Q7 | OS / WSL concepts | Short answer | 6 | ★ High — own words |
| Q8 | AI literacy + reflection | Short answer | 7 | ★ High — reflection is personal |
| **Total** | | | **44** | |

**Recommended pass: 26/44 (~60%).**
**Hard gate:** the learner must score **≥ 4 of 6 on Q1** (environment actually
works, or an honest, specific account of what is missing). There are no pure
multiple-choice marks in this version — a pass cannot be earned by recognition
alone.

---

## Q1 — Prove Your Environment Works (6)

- **(a)** 2 — real `python --version` / `python3 --version` output showing a 3.x
  version. Award 1 if output is present but ambiguous/partial. **Also award full
  2** for an honest, specific account that Python isn't installed yet plus what
  they'd install — this is a valid starting-point answer, not a failure.
- **(b)** 2 — real `conda env list` output **OR** an honest, specific statement
  that conda is not yet installed plus what they'd install (Miniconda/Anaconda).
  Award 0 for blank or obviously fabricated output (e.g. mismatched prompt style).
- **(c)** 2 — correctly reads the version meaning AND names a real way to check a
  package (`pip list`, `conda list`, `pip show pandas`, `python -c "import pandas"`).
  1 mark for one of the two.

> Assessor note: the signal here is *whether the environment runs at all*, not
> the version number. A messy-but-real transcript scores full marks.

## Q2 — What Environment Are You In? (5)

- **(a)** 2 — real shell output (`/bin/bash`, `/bin/zsh`, PowerShell version, etc.).
- **(b)** 2 — correct OS (1) + correct identification of WSL vs native vs PowerShell
  with a plausible "how I can tell" (1).
- **(c)** 1 — any concrete, correct reason (different commands, path syntax
  `C:\` vs `/`, package managers, line endings, `touch`/`ls` not native to old
  PowerShell, etc.).

## Q3 — CLI Navigation + Predict (6)

- **(a)** 1 — `cd projects/sctp` (accept `cd ~/projects/sctp`, absolute path).
- **(b)** 2 — `pwd` → `/home/user/projects/sctp` (1); `ls` → `data.csv` (1).
- **(c)** 2 — `mkdir output` (1) + `cd ..` (1).
- **(d)** 1 — recognises the folder doesn't exist / wrong location, and names
  `ls` (or `ls -a`, `pwd`) to inspect.

## Q4 — Read and Predict Output (4)

- **(a)** 1 — `17` (8 + 9).
- **(b)** 1 — "sums the numbers greater than 4" (or equivalent plain English).
- **(c)** 2 — Line 1 `Hello, world!` (1); Line 2 `Hello, Ada!` (1).

## Q5 — Find and Fix the Bug (4)

- **(a)** 1 — returns `3`, but those are the **odd** numbers (1,3,5); `% 2 == 1`
  matches odds, not evens. Award the mark for identifying odd-vs-even confusion.
- **(b)** 2 — corrected function uses `n % 2 == 0` and returns the count (full 2).
  1 mark if logic right but minor structural slip.
- **(c)** 1 — "checks whether n divides evenly by 2 / has no remainder / is even".

## Q6 — Git Workflow (6)

- Step 1: 1 — `git branch my-solutions` / `git checkout -b my-solutions` / `git switch -c my-solutions`.
- Step 2: 1 — `git checkout my-solutions` / `git switch my-solutions` (waive if step 1 already created+switched and they note it).
- Step 3: 1 — `git add q4.py`.
- Step 4: 1 — `git commit -m "Add Q4 answers"`.
- Step 5: 1 — `git push origin my-solutions`.
- Step 6 (short answer): 1 — "the file is modified but not staged" + `git add <file>`.

## Q7 — OS / WSL Concepts (6, 2 each)

- **(a)** Kernel = core of the OS that manages hardware (CPU/memory/devices) and
  mediates between software and hardware. 2 full / 1 partial / 0 wrong.
- **(b)** **Not accurate.** WSL is not two fully independent OSes; WSL 2 runs a
  real Linux kernel inside a lightweight, tightly-integrated VM that shares files
  and resources with Windows. Full 2 for "not accurate" + correct reason; 1 for
  "not accurate" with weak/no reason.
- **(c)** Terminal emulator = the window/app (Windows Terminal, iTerm2, GNOME
  Terminal); shell = program interpreting commands (bash, zsh, PowerShell);
  ≥1 example of each. 2 full / 1 partial.

## Q8 — AI Literacy + Self-Directed Learning (7)

- **(a)** 3 — 1 for choosing B (or well-justified A); 1 per valid reason (max 2):
  defined role, explicit steps, stated audience/constraints, structured format.
- **(b)** 1 — genuine strength of Prompt A: natural context, realistic, richer
  background.
- **(c)** 3 — the diagnostic gold:
  - 1: names a *specific* thing they didn't know.
  - 1: describes a concrete way they resolved it (named resource/search/person).
  - 1: shows judgement — how they verified the answer was correct (tested it, it
    worked, cross-checked docs). Generic "I just asked ChatGPT" with no
    verification = 0 on this third mark.

---

## Interpreting results (for instructors)

- **Strong Q1/Q2, weak elsewhere:** environment is set up; coach on concepts. Good sign.
- **Weak Q1/Q2 but strong written items:** recognises concepts but likely hasn't
  actually got a working setup — prioritise hands-on onboarding.
- **Weak Q8(c):** flag for the self-directed-learning support the programme emphasises.
