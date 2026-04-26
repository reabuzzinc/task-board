# CLAUDE.md — Task Board Project

## Project Overview

React-based task board application built with Vite.

**Features:**
- Add tasks via text input (Enter key or button)
- Toggle completion with checkboxes
- Delete tasks
- Completed tasks displayed in gray with strikethrough

**Stack:** React 19, Vite, CSS (no UI library)

---

## Git Operation Rules

### Push to GitHub on Every Code Change

**After every meaningful code change, always commit and push to GitHub.**

Workflow to follow each time:

```bash
git add <changed files>
git commit -m "<concise message describing the change>"
git push origin <current-branch>
```

Rules:
- Stage specific files by name — never `git add -A` or `git add .` blindly (risk of committing secrets or binaries).
- Write commit messages in the imperative: "Add login page", "Fix task deletion bug", not "Added" or "Fixed".
- Do **not** force-push to `main`/`master` under any circumstances.
- Do **not** skip pre-commit hooks (`--no-verify`).

### Branch Strategy

- `main` — production-ready code only.
- Feature work goes on short-lived branches: `feature/<topic>`.
- Merge to `main` via Pull Request; do not push directly unless explicitly told to.

### Commit Message Format

```
<type>: <short summary>  (50 chars max)

<optional body — wrap at 72 chars>
```

Types: `feat`, `fix`, `refactor`, `style`, `test`, `docs`, `chore`.

---

## Development Guidelines

- Prefer editing existing files over creating new ones.
- Do not add error handling or abstractions beyond what the task requires.
- Do not add comments unless the **why** is non-obvious.
- Run `npm run dev` to verify UI changes before committing.

---

## Environment

- Platform: Windows 11
- Shell: bash (Unix syntax in commands)
- Working directory: `c:\claudeAI\task-board`
- Remote: https://github.com/reabuzzinc/task-board.git
