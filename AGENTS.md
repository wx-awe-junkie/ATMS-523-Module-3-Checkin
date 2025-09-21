# Repository Guidelines

This repository is a lightweight course module scaffold. Keep changes small, readable, and easy to review. Use the structure and conventions below to maintain consistency as the project grows.

## Project Structure & Module Organization
- `src/` – Source code organized by feature (e.g., `src/data/`, `src/models/`).
- `notebooks/` – Jupyter notebooks for exploration; keep outputs cleared.
- `tests/` – Unit tests mirroring `src/` layout (e.g., `tests/data/test_loader.py`).
- `scripts/` – One-off CLI utilities; keep pure functions in `src/`.
- `data/` – Local-only; add `data/.gitignore` (do not commit raw data).
- `docs/` – Lightweight docs, figures, and architecture notes.

## Build, Test, and Development Commands
- Environment: `python -m venv .venv && source .venv/bin/activate`
- Install: `pip install -U pip && pip install -r requirements.txt` (or `pip install -e .` if a package is defined).
- Run tests: `pytest -q` (add `-k name` to filter; `-x` to stop early).
- Lint/format: `ruff check .` and `ruff format .` (or `black .` and `isort .`).
- Run app/notebook: `python -m src.<module>` or `jupyter lab` in `notebooks/`.

## Coding Style & Naming Conventions
- Python 3.10+; follow PEP 8. Use type hints and `mypy` for strict code paths.
- Format with `ruff format` (or `black`); import order via `ruff`/`isort`.
- Naming: modules `snake_case.py`, classes `CamelCase`, functions/vars `snake_case`.
- Keep functions small; prefer pure functions in `src/` and thin CLIs in `scripts/`.

## Testing Guidelines
- Framework: `pytest` with `pytest-cov` for coverage. Aim for ≥80% on changed lines.
- Test files: `tests/<area>/test_<unit>.py`; name tests `test_<behavior>()`.
- Use fixtures for I/O; avoid network/file system in unit tests unless mocked.

## Commit & Pull Request Guidelines
- Commits: use Conventional Commits (e.g., `feat: add loader`, `fix: handle NaN`).
- PRs: concise title, summary of changes, linked issue (if any), and before/after notes or screenshots for user-facing updates. Keep PRs under ~300 LOC where feasible.

## Security & Configuration
- Do not commit secrets. Use `.env` (ignored) and document required variables in `docs/CONFIG.md`.
- Large files/data remain local; add patterns to `.gitignore` (e.g., `data/`, `*.ipynb_checkpoints`).

## Agent-Specific Notes
- Follow this file’s conventions for any edits. Prefer `rg` for search, keep patches minimal, and avoid unrelated changes. Add or update docs/tests alongside code.
