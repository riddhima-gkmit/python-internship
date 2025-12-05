# Git Commands

**Git** is a distributed version control system used to track changes, manage branches, and collaborate on code efficiently.

## Command Reference

| **Git Command / Concept**             | **Explanation**                                                                                               |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `git clone <repo-url>`                | Copy (clone) a remote repository to your local machine.                                                       |
| `git pull`                            | Fetch and merge the latest changes from the remote repository into your current branch.                       |
| `git push`                            | Upload your local commits to the remote repository.                                                           |
| `git status`                          | Show changed, staged, and untracked files.                                                                    |
| `git add <file>`                      | Stage changes to be included in the next commit.                                                              |
| `git commit -m "<message>"`           | Save staged changes with a clear commit message.                                                              |
| **Commit naming**                     | Follow meaningful, conventional commit messages (e.g., `feat: add login handler`, `fix: correct null check`). |
| `git branch <name>`                   | Create a new branch for isolated work.                                                                        |
| **Feature branching**                 | Use branches like `feature/login-flow` or `fix/payment-timeout` for organized development.                    |
| `git checkout <branch>`               | Switch to a different branch.                                                                                 |
| `git switch <branch>`                 | A modern, safer command for switching branches.                                                               |
| `git merge <branch>`                  | Merge changes from another branch into your current one.                                                      |
| `git rebase <branch>`                 | Reapply your changes on top of another branch for a cleaner history.                                          |
| `git cherry-pick <commit>`            | Apply a specific commit from one branch onto another.                                                         |
| `git stash`                           | Temporarily save uncommitted work without committing it.                                                      |
| `git stash pop`                       | Restore stashed changes and remove them from the stash list.                                                  |
| `git log`                             | View commit history.                                                                                          |
| `git diff`                            | Compare changes not yet staged or committed.                                                                  |
| `git revert <commit>`                 | Create a new commit that reverses a previous one.                                                             |
| `git reset --soft / --mixed / --hard` | Move branch pointers or discard changes (dangerous—use carefully).                                            |
| **Conflict resolution**               | Manually resolve merge/rebase conflicts and mark them resolved with `git add`.                                |
| **Squashing** (`git rebase -i`)       | Combine multiple commits into one clean, readable commit before merging.                                      |
