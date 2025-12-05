# Poetry Commands

**Poetry** is a Python tool that manages project dependencies, virtual environments, and packaging through a simple and unified interface.

## Command Reference

| **Poetry Command** | **Explanation** |
|--------------------|-----------------|
| `poetry --version` | Show the version of your Poetry installation. |
| `poetry new <project>` | Create a new Poetry project with a standard directory structure. |
| `poetry init` | Add Poetry to an existing project and interactively create a `pyproject.toml` file. |
| `poetry run <command>` | Execute a command inside the virtual environment managed by Poetry. |
| `poetry add <package>` | Add a package to `pyproject.toml` and install it. |
| `poetry update` | Update your project’s dependencies to their latest allowed versions. |
| `poetry install` | Install all dependencies listed in `pyproject.toml` / `poetry.lock`. |
| `poetry show` | List installed packages and their versions. |
| `poetry lock` | Generate or refresh the `poetry.lock` file, locking dependency versions. |
| `poetry lock --no-update` | Recreate `poetry.lock` without upgrading any dependency versions. |
| `poetry check` | Validate that `pyproject.toml` is well-formed. |
| `poetry config --list` | Show Poetry’s current configuration settings. |
| `poetry env list` | List virtual environments created by Poetry for the project. |
| `poetry export` | Export `poetry.lock` to alternative formats (e.g., `requirements.txt`). |
