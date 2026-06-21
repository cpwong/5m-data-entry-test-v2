# Answer Key and Marking Rubric

**For assessor use only — do not share with learners.**

---

## Scoring Summary

| Question | Topic | Format | Marks |
|----------|-------|--------|-------|
| Q1 | Python: Variables & Constants | MCQ (3 parts) | 3 |
| Q2 | Python: Packages & Conda | MCQ (3 parts) + stretch | 3 + 2 bonus |
| Q3 | CLI: Navigation | MCQ (4 parts) | 4 |
| Q4 | GitHub: Core Concepts | MCQ (4 parts) | 4 |
| Q5 | OS Concepts | MCQ (4 parts) | 4 |
| Q6 | OS: WSL & Terminals | Short answer (3 parts) | 6 |
| Q7 | AI Literacy | Short answer + rewrite | 6 |
| Q8 | Python: Loops & Functions | Code (2 tasks) | 4 |
| Q9 | CLI: Commands | Commands (6 steps) | 6 |
| Q10 | GitHub: Git Workflow | Commands (6 steps) | 6 |
| **Total** | | | **46 (+2 bonus)** |

**Pass threshold (recommended):** 28/46 (60%)

---

## Q1 — Python: Variables and Constants

**(a)** **B** — `MAX_RETRIES` and `PI` follow the Python convention for constants, but `1st_value` is not a valid identifier.

**(b)** **B** — Constants are a convention only; Python does not enforce immutability on ALL_CAPS names.

**(c)** **C** — `my_user_age` follows PEP 8 snake_case for regular variables.

---

## Q2 — Python: Packages, Environments, and Conda

**(a)** **A** — `conda install pandas`

**(b)** **B** — `.env` files store environment variables such as API keys.

**(c)** **B** — `conda env create -f environment.yml`

**(d)** *(Stretch — 2 bonus marks)*

```python
from dotenv import load_dotenv
import utils
```

Accept `load_dotenv()` call on a third line as an addition, not required. Do not penalise if learner also writes `load_dotenv()` below the import.

---

## Q3 — CLI: Basic Command Line Navigation

**(a)** **B** — `ls` (or `dir` on Windows Command Prompt)

**(b)** **B** — `cd ..`

**(c)** **C** — `mkdir data`

**(d)** **B** — Displays the full path of the current working directory.

---

## Q4 — GitHub: Core Concepts and Commands

**(a)** **B** — `git clone` downloads locally; forking creates a copy on GitHub.

**(b)** **C** — `git add <filename>`

**(c)** **C** — `git clone https://github.com/su-ntu-ctp/5m-data-entry-test.git`

**(d)** **C** — Shows the state of the working directory and staging area.

---

## Q5 — Operating System Concepts

**(a)** **B** — The kernel manages hardware resources and mediates between software and the CPU/memory/devices.

**(b)** **B** — WSL is a compatibility layer integrated into Windows, not a full VM.

**(c)** **B** — VMs emulate an entire separate computer with their own OS and kernel, with dedicated resource allocation.

**(d)** **B** — A terminal is the interface; a shell is the program that interprets and executes commands.

---

## Q6 — OS: WSL and Terminal Shells

### Rubric (2 marks each)

**(a)** Award 2 marks for a response that identifies:
- The application to open (e.g. Windows Terminal, Ubuntu app from Microsoft Store, or native Terminal on macOS/Linux)
- What happens on launch (a command prompt / shell session appears, ready to accept commands)

Award 1 mark if only one of the two elements is present. Award 0 for vague or incorrect responses.

**(b)** Award 2 marks for a response that correctly states:
- The claim is **not accurate**
- WSL does not give Linux its own separate kernel — WSL 2 uses a lightweight VM with a real Linux kernel that runs alongside Windows, but it is not "two completely separate operating systems" in the traditional sense; they share resources and integrate tightly

Award 1 mark if the learner correctly says "not accurate" but the explanation is incomplete or imprecise.

**(c)** Award 2 marks for a response that includes:
- A **terminal emulator** is the GUI window/application (e.g. Windows Terminal, iTerm2, GNOME Terminal)
- A **shell** is the program running inside it that interprets commands (e.g. bash, zsh, PowerShell)
- At least one example of each

Award 1 mark if the distinction is partially correct or only one example is given.

---

## Q7 — AI Literacy: Prompt Engineering

### Rubric

**Task 1(a)** — 1 mark for selecting **B** (or a well-reasoned case for A — accept with justification).

**Task 1(b)** — 1 mark per valid reason (max 2). Valid reasons include:
- Prompt B has a defined role, which anchors the AI's perspective
- Prompt B breaks the task into explicit steps, reducing ambiguity
- Prompt B specifies the audience and constraints, shaping tone and length
- Prompt B uses structured formatting, which is easier for the model to parse

**Task 1(c)** — 1 mark for identifying a genuine strength of the unchosen prompt. For Prompt A: natural context-setting, provides richer background, reads as a realistic user request.

**Task 2** — Award up to 3 marks:
- 1 mark: the rewritten prompt is coherent and represents an actual improvement
- 1 mark: the borrowed element is clearly identified
- 1 mark: the explanation of *why* it improves the prompt is specific and accurate

---

## Q8 — Python: Loops and Functions

**Task 1** — Award 2 marks for a correct `count_evens` function:
- Uses a loop (for or while) — 1 mark
- Correctly identifies even numbers using `% 2 == 0` and counts them — 1 mark

Award 1 mark if the function structure is correct but logic is slightly off (e.g. counts odds instead). Award 0 for no loop or no return.

**Task 2** — Award 2 marks:
- Calls `count_evens([10, 15, 20, 33, 42, 57, 64])` correctly — 1 mark
- Prints `Even numbers found: 4` in the correct format — 1 mark

Accept f-string, `.format()`, or `+` concatenation as valid print approaches.

---

## Q9 — CLI: Directory Navigation and File Creation

Award 1 mark per correct command (6 total). Accept minor variations.

| Step | Accepted answer(s) |
|------|--------------------|
| 1 | `cd Documents` or `cd ~/Documents` |
| 2 | `mkdir sctp-project` |
| 3 | `cd sctp-project` |
| 4 | `touch notes.txt` (Linux/macOS/WSL) or `New-Item notes.txt` (PowerShell) |
| 5 | `pwd` |
| 6 | `cd ~` or `cd` (bare) or `cd /home/user` |

---

## Q10 — GitHub: Git Workflow

Award 1 mark per correct command (6 total).

| Step | Accepted answer(s) |
|------|--------------------|
| 1 | `git clone https://github.com/su-ntu-ctp/5m-data-entry-test.git` |
| 2 | `git branch my-solutions` or `git checkout -b my-solutions` or `git switch -c my-solutions` |
| 3 | `git checkout my-solutions` or `git switch my-solutions` (if step 2 used `git branch`) |
| 4 | `git add q8.py` |
| 5 | `git commit -m "Add Q8 solution"` |
| 6 | `git push origin my-solutions` |

Note: if learner used `git checkout -b my-solutions` in step 2, step 3 is already implied — award full marks if they note this or skip step 3 with a comment.
