# Git Commands Cheat Sheet

## Configuration
- **Set user name**: `git config --global user.name "Your Name"`
- **Set user email**: `git config --global user.email "you@example.com"`
- **Check configuration**: `git config --list`

## Repository Management
- **Initialize a new repository**: `git init`
- **Clone an existing repository**: `git clone <repository-url>`

## Working with Changes
- **Check status**: `git status`
- **Stage changes**: `git add <file>` or `git add .` (for all files)
- **Commit changes**: `git commit -m "Commit message"`
- **View commit history**: `git log`
- **View changes**: `git diff`

## Branching
- **List local branches**: `git branch`
- **List remote branches**: `git branch -r`
- **List all branches (local and remote)**: `git branch -a`
- **Create a new branch**: `git branch <branch-name>`
- **Switch branches**: `git checkout <branch-name>` or `git switch <branch-name>`
- **Create and switch to a new branch**: `git checkout -b <branch-name>`
- **Merge a branch**: `git merge <branch-name>`
- **Delete a local branch**: `git branch -d <branch-name>`
- **Delete a remote branch**: `git push origin --delete <branch-name>`

## Remote Repositories
- **Add a remote**: `git remote add <name> <url>`
- **View remotes**: `git remote -v`
- **Fetch changes**: `git fetch`
- **Pull changes**: `git pull`
- **Push changes**: `git push`

## Undoing Commits Not Yet Pushed
- **Undo the most recent commit but keep the changes in your working directory**: `git reset --soft HEAD~1`
- **Undo the most recent commit and discard the changes**: `git reset --hard HEAD~1`
- **Remove a specific commit using interactive rebase**: `git rebase -i HEAD~n` (replace `n` with the number of commits to go back, and follow the interactive editor instructions)
- **Revert to a specific commit using reflog**:
  1. View commit history with: `git reflog`
  2. Reset to the desired commit with: `git reset --hard <commit-hash>`
