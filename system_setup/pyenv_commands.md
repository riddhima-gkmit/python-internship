# pyenv Commands

**pyenv** is used to install and manage multiple Python versions on your system.

## Command Reference

| **pyenv Command** | **Explanation** |
|-------------------|-----------------|
| `pyenv --version` | Show the installed version of pyenv. |
| `pyenv install --list` | List all available Python versions you can install. |
| `pyenv install <version>` | Install a specific Python version (e.g., `pyenv install 3.11.6`). |
| `pyenv uninstall <version>` | Remove an installed Python version. |
| `pyenv versions` | List all Python versions pyenv is managing. |
| `pyenv global <version>` | Set the global (system-wide) Python version. |
| `pyenv local <version>` | Set the local Python version for the current project directory (creates a `.python-version` file). |
| `pyenv shell <version>` | Set the Python version only for the current shell session. |
| `pyenv rehash` | Rebuild shims (usually automatic). |
| `pyenv which <command>` | Show the full path of an executable that pyenv is referencing. |
| `pyenv doctor` | Diagnose issues with pyenv setup (requires plugin). |
| `pyenv update` | Update pyenv and its plugins (requires update plugin). |
