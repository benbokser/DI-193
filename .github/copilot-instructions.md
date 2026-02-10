# Copilot instructions for this repository

Purpose: Help AI coding agents be immediately productive in this small teaching repository of beginner Python exercises (notebooks + one script).

Quick repo summary
- Small learning repo containing interactive notebooks and one script: [num_game.ipynb](num_game.ipynb), [lists_dicts.ipynb](lists_dicts.ipynb), [lists_exercise.ipynb](lists_exercise.ipynb), [python_intro_ex_1.py](python_intro_ex_1.py), and [welcome.txt](welcome.txt).
- Primary intent: student exercises and short scripts — avoid large-scale refactors or converting notebooks to production packages unless the user asks.

What the agent should do first
- Inspect the notebooks named above to understand exercise intent before editing.
- Prefer creating small helper `.py` modules alongside notebooks instead of editing student cells directly.
- If changing a notebook, keep changes minimal and explain them in the PR message.

Execution & debugging
- Notebooks: open in Jupyter / VS Code Notebook UI to run and validate interactively.
- Scripts: run on Windows PowerShell with `python python_intro_ex_1.py` (or `python3` if configured that way).
- There are no test files or build steps present — run examples manually after edits.

Project-specific conventions
- Preserve notebook cell metadata and student content; do not remove `metadata.id` entries or rewrite all cells.
- Keep changes small and focused: one concept fix per commit/PR.
- Avoid adding unnecessary dependencies. If a dependency is required, add a `requirements.txt` at repo root and call it out in PR notes.

Patterns and examples
- Random-number exercise: [num_game.ipynb](num_game.ipynb) uses only the standard library (`random`). Example safe change: fix input type handling by adding `int()` conversion in a new helper cell rather than rewriting unrelated cells.
- If converting a notebook snippet into reusable code, place it in a new module file (e.g., `exercises/num_game.py`) and leave a short cell in the notebook that imports and calls the module.

Integration & external dependencies
- Current notebooks rely only on Python standard library. No CI, no database, no external services.
- If you add integrations (APIs, packages), include rationale and a minimal reproducible example in the same PR.

When to ask the user
- Before making structural changes (moving notebooks into packages, adding CI, or introducing tests).
- If a notebook appears to be student-submitted work and you plan to substantially edit or normalize it.

If you find an existing `.github/copilot-instructions.md` or agent file elsewhere
- Merge conservatively: preserve any explicit developer instructions, keep this file focused on quick context and safe editing patterns.

Contact / feedback
- After making edits, open a short PR description explaining the change, run the affected notebook locally, and ask the user to verify interactive behavior.

End of instructions.