# uv Commands (Astral’s uv)

**uv** is a fast Python package manager, virtual environment manager, and pip replacement.

## Command Reference

| **uv Command** | **Explanation** |
|----------------|-----------------|
| `uv --version` | Show the installed uv version. |
| `uv init` | Create a new project with a `pyproject.toml`. |
| `uv venv` | Create a virtual environment quickly (replacement for `python -m venv`). |
| `uv venv --python <version>` | Create a venv with a specific Python interpreter. |
| `uv run <command>` | Run a command inside the environment (auto-creates venv if missing). |
| `uv add <package>` | Add a dependency and update `pyproject.toml` + lockfile. |
| `uv remove <package>` | Remove a dependency. |
| `uv install` | Install all dependencies from the lockfile. |
| `uv sync` | Sync environment with lockfile (like `poetry install`). |
| `uv lock` | Generate or update the `uv.lock` lockfile. |
| `uv tree` | Show the dependency tree. |
| `uv pip install <pkg>` | Use uv as a fast drop-in replacement for pip. |
| `uv pip list` | List installed packages (uv-optimized pip). |
| `uv python install <version>` | Install Python (uv has built-in Python installations like pyenv). |
| `uv python list` | List available Python versions. |
| `uv python versions` | List installed Python versions. |
| `uv python uninstall <version>` | Uninstall an installed Python version. |
