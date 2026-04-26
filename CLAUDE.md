# CLAUDE.md — Task Board Project

## Project Overview

This is a task board application. Update this section as the project takes shape.

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
- If the repository has not been initialized yet, run `git init` first, then set the remote:
  ```bash
  git init
  git remote add origin <GitHub repository URL>
  git push -u origin main
  ```

### Branch Strategy

- `main` — production-ready code only.
- Feature work goes on short-lived branches: `feature/<topic>`.
- Merge to `main` via Pull Request; do not push directly unless the branch has no protection rules and the user explicitly says so.

### Commit Message Format

```
<type>: <short summary>  (50 chars max)

<optional body — wrap at 72 chars>
```

Types: `feat`, `fix`, `refactor`, `style`, `test`, `docs`, `chore`.

---

## Development Guidelines

- Prefer editing existing files over creating new ones.
- Do not add error handling, fallbacks, or abstractions beyond what the task requires.
- Do not add comments unless the **why** is non-obvious.
- Run tests (if they exist) before committing.

---

## Environment

- Platform: Windows 11
- Shell: bash (Unix syntax in commands)
- Working directory: `c:\claudeAI\task-board`
