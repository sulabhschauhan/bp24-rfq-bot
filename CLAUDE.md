# CLAUDE.md — Working Rules

Rules for all Claude Code sessions in this repo.

- Read the task from `prompts/<NN>_task.md`. Write all results to `outputs/<NN>_output.md`. Never dump results to the terminal only.
- One task per prompt, one file per prompt. Surgical edits only — never rewrite a whole file unless explicitly told to.
- Do not read files not named in the task.
- Never commit secrets. Credentials live in `.env`, which is gitignored.
- No LLM-generated SQL anywhere in this project. All database queries are built deterministically in Python.
- All LLM output must pass through a Pydantic validation layer before being used downstream.
- Append one line to `SESSION_LOG.md` after each completed task: date | task number | one-line summary | files touched.
