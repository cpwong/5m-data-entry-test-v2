# Answer Key and Marking Rubric

**For assessor use only. Do not share with learners.**

---

## Scoring Summary

| Question | Topic | Format | Marks |
|----------|-------|--------|-------|
| Q1 | Mixed MCQ: Python, CLI, Git, OS, shells (15 parts) | MCQ | 15 |
| Q2 | Python & Environment Setup | Paste output + short answer | 10 |
| Q3 | Your Operating System and Shell | Paste output + short answer | 10 |
| Q4 | CLI: Navigation and Predicting Output | Commands + predict | 10 |
| Q5 | Operating Systems, Terminals, and Shells | Short answer (3 parts) | 10 |
| Q6 | AI Literacy: Prompt Engineering | Short answer + rewrite | 15 |
| Q7 | Python: Read and Predict Output | Predict + short answer | 10 |
| Q8 | Python: Find and Fix the Bug | Code + short answer | 10 |
| Q9 | GitHub: Git Workflow | Commands + short answer | 10 |
| **Total** | | | **100** |

**Pass threshold (recommended):** 60/100 (60%).

> **Optional hard gate (recommended):** require a minimum of 6/10 on Q2 so a learner cannot pass purely on MCQ recognition without a working environment (or an honest, specific account of what is missing). The programme team should confirm or remove this gate before publishing.

---

## Q1 — Multiple Choice: Core Concepts (15 parts, 1 mark each)

| # | Answer | Note |
|---|--------|------|
| 1 | **B** | `1st_value` is invalid (identifier cannot start with a digit). |
| 2 | **B** | Constants are convention only; Python does not enforce immutability on ALL_CAPS names. |
| 3 | **C** | PEP 8 snake_case for regular variables. |
| 4 | **A** | `conda install pandas`. |
| 5 | **B** | `.env` stores environment variables such as API keys. |
| 6 | **B** | `conda env create -f environment.yml`. |
| 7 | **B** | `ls` (or `dir` on Windows Command Prompt). |
| 8 | **B** | `cd ..` moves up one level. |
| 9 | **C** | `mkdir data`. |
| 10 | **B** | `pwd` prints the working directory path. |
| 11 | **B** | `clone` is local; forking creates a GitHub-side copy. |
| 12 | **C** | `git clone <url>`. |
| 13 | **C** | State of working directory and staging area. |
| 14 | **B** | Kernel manages hardware and mediates between software and CPU/memory/devices. |
| 15 | **B** | Terminal is the interface; shell is the program interpreting commands. |

---

## Q2 — Python & Environment Setup (10 marks)

**(a) + (b) Pasted terminal output (6 marks)**

- **2 marks**: real Python version output (`Python 3.x.y`), **or** a clear, specific honest statement that Python is not installed plus what they would install.
- **2 marks**: real `conda env list` output showing env names and paths, **or** a clear, specific honest statement that conda is not installed plus what they would install (Miniconda / Anaconda).
- **2 marks**: commands shown alongside output (not just bare version numbers); output looks genuine (env paths, prompt artefacts, terminal noise).

Honesty-about-not-installed answers earn full marks if specific. Penalise output that looks copy-pasted from documentation (generic `Python 3.x.x`, no env paths, perfectly clean).

**(c) Short answer (4 marks)**

- **2 marks**: what the version number tells them (which Python interpreter is active; major.minor.patch).
- **2 marks**: at least one valid way to check whether `pandas` is installed: `pip list`, `pip show pandas`, `conda list pandas`, `python -c "import pandas"`.

Award 1 mark per half if the answer is on-track but incomplete.

---

## Q3 — Your Operating System and Shell (10 marks)

**(a) Pasted shell output (2 marks)**

Award 2 marks for genuine output of `echo $SHELL` (e.g. `/bin/bash`, `/usr/bin/zsh`) or `$PSVersionTable.PSVersion`. Accept "not installed" if honest and specific. 1 mark for partial/ambiguous output.

**(b) OS + terminal identification (4 marks)**

- **2 marks**: specific OS version (e.g. "Windows 11 23H2", "macOS Sonoma 14.4", "Ubuntu 22.04"). 1 mark for vague ("Windows", "Mac").
- **2 marks**: correctly identifies the terminal type (WSL / native / PowerShell) **and** gives a tell (e.g. `/bin/bash` path → WSL or Linux; `$PSVersionTable` exists → PowerShell; macOS default `/bin/zsh`). 1 mark for identification without a tell.

**(c) Why PowerShell breaks POSIX course instructions (4 marks)**

Award 4 marks for a concrete, correct, specific example. The question is answerable from general knowledge; do not penalise candidates for not having used PowerShell themselves. Acceptable answers include:
- Different commands (`touch`, `grep`, `which` missing in PowerShell without aliases/modules).
- Path separators (`/` vs `\`).
- Environment variable syntax (`$VAR` vs `$env:VAR`).
- Bash scripts will not run; activation scripts behave differently.
- Tool availability assumes a POSIX shell.

Award 2 marks for a vague but pointed-in-the-right-direction answer ("the commands are different"). Award 0 for "they look different" with no example.

---

## Q4 — CLI Navigation and Predicting Output (10 marks)

**(a) Single command (2 marks)**

Accept: `cd projects/sctp`, `cd ./projects/sctp`, or `cd /home/user/projects/sctp`.

**(b) Predict pwd and ls output (4 marks)**

- **2 marks**: `pwd` output is `/home/user/projects/sctp`.
- **2 marks**: `ls` output is `data.csv`.

**(c) mkdir + cd up (2 marks)**

Accept either separate or combined commands:
- `mkdir output` then `cd ..`
- `mkdir output && cd ..`

Both intents must be present. 1 mark for one of the two.

**(d) Diagnose error (2 marks)**

- **1 mark**: what the error means (`reports` does not exist in the current directory, or it is not a directory).
- **1 mark**: a command to inspect contents: `ls` (also accept `ls -la`, `dir` in PowerShell).

---

## Q5 — Operating Systems, Terminals, and Shells (10 marks)

**(a) What is a kernel (3 marks)**

Award up to 3 marks for an own-words explanation covering:
- **1 mark**: it is the core of the operating system.
- **1 mark**: it mediates between software (apps) and hardware (CPU, memory, devices).
- **1 mark**: the answer is in the learner's own words, not a textbook paraphrase or a copy of the Q1 option B wording.

**(b) WSL misconception (4 marks)**

Award up to 4 marks:
- **1 mark**: explicitly says the claim is **not accurate**.
- **2 marks**: explains that WSL 2 runs a real Linux kernel inside a lightweight VM tightly integrated with Windows (file/resource interop).
- **1 mark**: articulates why "two completely separate operating systems" overstates the separation (shared resources, integrated filesystem).

**(c) Terminal emulator vs shell (3 marks)**

- **1 mark**: terminal emulator: GUI window/application (Windows Terminal, iTerm2, GNOME Terminal).
- **1 mark**: shell: program running inside it that interprets commands (bash, zsh, PowerShell).
- **1 mark**: at least one valid example given for **each** of the two.

---

## Q6 — AI Literacy: Prompt Engineering (15 marks)

**Task 1**

- **(a) 2 marks**: selecting **B** (or a well-reasoned, defensible case for A; accept A only with strong justification).
- **(b) 4 marks**: 2 marks per valid reason (max 2 reasons). Valid reasons include:
  - Prompt B has a defined role, anchoring the AI's perspective.
  - Prompt B breaks the task into explicit numbered steps, reducing ambiguity.
  - Prompt B specifies audience and constraints, shaping tone and length.
  - Prompt B uses structured formatting, easier for the model to parse.
  
  Award 1 mark for a reason that is correct but vaguely stated.
- **(c) 3 marks**: genuine strength of the unchosen prompt. For Prompt A: natural context-setting, richer background, reads as a realistic user request, demonstrates the kind of unstructured input AI must often parse. Award 1-2 marks for partially correct answers.

**Task 2 — Rewrite (6 marks)**

- **2 marks**: rewritten prompt is coherent and represents an actual improvement on the original.
- **2 marks**: the borrowed element is clearly identified.
- **2 marks**: the explanation of *why* it improves the prompt is specific and accurate.

---

## Q7 — Python: Read and Predict Output (10 marks)

**Snippet 1**

- **(a) 3 marks**: answer is **`17`** (sums 8 + 9; only values strictly greater than 4). Award 1 mark for `21` (off-by-one threshold, included 4) or other near-misses that show some understanding. 0 for guesses.
- **(b) 3 marks**: describes that the loop sums all numbers in the list that are greater than 4. Award 2 marks for "sum of large numbers" without naming the threshold; 1 mark for any partially correct description.

**Snippet 2**

- **(c) 4 marks**: both lines correct, 2 marks each:
  - Line 1: `Hello, world!`
  - Line 2: `Hello, Ada!`
  
  Deduct 1 mark per line for: missing comma, missing exclamation mark, missing space after comma, or wrong capitalisation. Floor 0 per line.

---

## Q8 — Python: Find and Fix the Bug (10 marks)

**Test input:** `[1, 2, 3, 4, 5, 6, 8]`. Buggy version returns `3` (odds: 1, 3, 5); correct version returns `4` (evens: 2, 4, 6, 8).

**(a) Diagnose (3 marks)**

- **1 mark**: correctly states the buggy version returns `3`.
- **2 marks**: explains the cause: `n % 2 == 1` matches **odd** numbers, not even.

Partial: 1 mark if they identify "wrong condition" without specifying odd-vs-even.

**(b) Fix (5 marks)**

Award up to 5 marks for a corrected function:
```python
def count_evens(numbers):
    count = 0
    for n in numbers:
        if n % 2 == 0:
            count = count + 1
    return count
```
- **3 marks**: correct logic (`% 2 == 0`).
- **1 mark**: correctly returns the count.
- **1 mark**: code is clean and would run as written.

Accept equivalent one-liners: `return sum(1 for n in numbers if n % 2 == 0)` or `return len([n for n in numbers if n % 2 == 0])` for full marks. Award 2 marks for any correct logic that fails to return a value, or returns the count of odds.

**(c) Explain (2 marks)**

Award 2 marks for: `n % 2 == 0` checks whether `n` is divisible by 2 with no remainder, i.e. whether `n` is even. Award 1 mark for partial phrasing ("checks if even" without explaining `%`).

---

## Q9 — GitHub: Git Workflow (10 marks)

**Steps 1 to 5: commands (8 marks)**

| Step | Marks | Accepted answer(s) |
|------|-------|--------------------|
| 1 | 2 | `git branch my-solutions` **or** `git checkout -b my-solutions` **or** `git switch -c my-solutions`. Award 1 mark for a syntactically wrong but conceptually correct attempt (e.g. `git new-branch`). |
| 2 | 1 | `git checkout my-solutions` **or** `git switch my-solutions`. Waive (award full) if step 1 used `git checkout -b` or `git switch -c` and the learner notes this in a comment or skips the step. |
| 3 | 1 | `git add q4.md`. |
| 4 | 2 | `git commit -m "Add Q4 answers"`. Award 1 mark for correct command but wrong/missing message. |
| 5 | 2 | `git push origin my-solutions` (also accept `git push -u origin my-solutions`). Award 1 mark for `git push` with no branch. |

**Step 6: short answer (2 marks)**

- **1 mark**: what `Changes not staged for commit` means (the file has been modified but is not yet in the staging area / index).
- **1 mark**: the command that stages it: `git add <file>`.
