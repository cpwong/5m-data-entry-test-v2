# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is the **SCTP Advanced Professional Certificate in Data Science and AI** technical entry assessment (v2). It is a static set of question files that candidates fork, fill in, and push back to GitHub — there is no build system, test suite, or runtime. The `.py` files (q8–q10) are answer templates, not executable programs to run as a whole.

## Layout

- `src/` — the 9 questions candidates answer (q1–q6 are `.md`, q7–q9 are `.py`). This is the canonical, current version.
- `answers/answer-key.md` — instructor answer key for `src/`. Keep in sync with `src/` when questions change.
- `.proposed-feng/` — a draft next version of the assessment with its own `src/` and `answers/`. Treat as a parallel work-in-progress; do not conflate with the live `src/`.
- `README.md` — candidate-facing instructions (fork → clone → edit `src/` → push → submit URL).

## Working in this repo

- When editing a question in `src/`, update the matching entry in `answers/answer-key.md` in the same change. The mapping is 1:1 by question number.
- `.proposed-feng/` mirrors the top-level structure (`src/` + `answers/`). Changes there are proposals and should not be cross-applied to the top-level `src/` unless explicitly requested.
- Question coverage by area is documented in `README.md` ("What This Assessment Covers" table) — preserve that mapping if renumbering questions.
