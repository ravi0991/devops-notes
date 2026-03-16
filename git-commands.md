# 📘 Git & GitHub Commands Reference Guide

This guide covers essential Git and GitHub CLI commands learned across
Days 22--26.

Sections included:

-   Setup & Configuration
-   Basic Workflow
-   Branching
-   Remote Repositories
-   Merging & Rebasing
-   Stash & Cherry Pick
-   Reset & Revert
-   GitHub CLI (gh) Commands

------------------------------------------------------------------------

# 1️⃣ Setup & Configuration

## git config

Configure Git username and email.

``` bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

Verify configuration:

``` bash
git config --list
```

------------------------------------------------------------------------

## git init

Initialize a new Git repository.

``` bash
git init
```

------------------------------------------------------------------------

## git clone

Clone an existing repository.

``` bash
git clone https://github.com/username/repository.git
```

------------------------------------------------------------------------

# 2️⃣ Basic Workflow

## git status

Check current state of repository.

``` bash
git status
```

------------------------------------------------------------------------

## git add

Add files to staging area.

Add single file:

``` bash
git add file.txt
```

Add all files:

``` bash
git add .
```

------------------------------------------------------------------------

## git commit

Save staged changes.

``` bash
git commit -m "Commit message"
```

------------------------------------------------------------------------

## git log

View commit history.

``` bash
git log
```

Compact view:

``` bash
git log --oneline
```

------------------------------------------------------------------------

## git diff

Show changes between commits, branches, or working directory.

``` bash
git diff
```

View staged changes:

``` bash
git diff --staged
```

------------------------------------------------------------------------

# 3️⃣ Branching

## git branch

List branches.

``` bash
git branch
```

Create branch:

``` bash
git branch feature-branch
```

------------------------------------------------------------------------

## git checkout

Switch branches.

``` bash
git checkout feature-branch
```

Create and switch:

``` bash
git checkout -b feature-branch
```

------------------------------------------------------------------------

## git switch

Modern alternative to checkout.

``` bash
git switch feature-branch
```

Create new branch:

``` bash
git switch -c feature-branch
```

------------------------------------------------------------------------

# 4️⃣ Remote Repositories

## git remote

View remote repositories.

``` bash
git remote -v
```

Add remote:

``` bash
git remote add origin https://github.com/user/repo.git
```

Update remote URL:

``` bash
git remote set-url origin NEW_URL
```

------------------------------------------------------------------------

## git push

Push commits to remote repository.

``` bash
git push origin main
```

Push new branch:

``` bash
git push -u origin feature-branch
```

------------------------------------------------------------------------

## git pull

Fetch and merge remote changes.

``` bash
git pull origin main
```

------------------------------------------------------------------------

## git fetch

Download changes without merging.

``` bash
git fetch origin
```

------------------------------------------------------------------------

## Fork (Concept)

Create a personal copy of someone else's repository on GitHub for
experimentation and contributions.

------------------------------------------------------------------------

# 5️⃣ Merging & Rebasing

## git merge

Merge feature branch into main branch.

``` bash
git checkout main
git merge feature-branch
```

------------------------------------------------------------------------

## git rebase

Reapply commits from one branch on top of another.

``` bash
git checkout feature-branch
git rebase main
```

------------------------------------------------------------------------

## Squash Commit vs Merge Commit

### Merge Commit

Preserves all commit history.

``` bash
git merge feature-branch
```

### Squash Commit

Combines commits into one.

``` bash
git merge --squash feature-branch
git commit -m "Squashed commit"
```

------------------------------------------------------------------------

# 6️⃣ Stash & Cherry Pick

## git stash

Temporarily save uncommitted changes.

``` bash
git stash
```

List stashes:

``` bash
git stash list
```

Apply stash:

``` bash
git stash apply
```

Remove stash:

``` bash
git stash drop
```

------------------------------------------------------------------------

## git cherry-pick

Apply a specific commit from another branch.

``` bash
git cherry-pick <commit-id>
```

Example:

``` bash
git cherry-pick a3f5d2b
```

------------------------------------------------------------------------

# 7️⃣ Reset & Revert

## git reset

Undo commits locally.

Soft reset:

``` bash
git reset --soft HEAD~1
```

Hard reset:

``` bash
git reset --hard HEAD~1
```

------------------------------------------------------------------------

## git revert

Create a new commit that undoes previous commit.

``` bash
git revert <commit-id>
```

------------------------------------------------------------------------

# 8️⃣ GitHub CLI (gh) Commands

## Authenticate GitHub CLI

``` bash
gh auth login
```

------------------------------------------------------------------------

## Create Repository

``` bash
gh repo create repo-name
```

------------------------------------------------------------------------

## Clone Repository

``` bash
gh repo clone username/repository
```

------------------------------------------------------------------------

## Create Pull Request

``` bash
gh pr create --title "Feature update" --body "Description"
```

------------------------------------------------------------------------

## View Pull Requests

``` bash
gh pr list
```

------------------------------------------------------------------------

## Merge Pull Request

``` bash
gh pr merge
```

------------------------------------------------------------------------

## Create GitHub Gist

``` bash
gh gist create file.sh --public --desc "Sample script"
```

------------------------------------------------------------------------

# 🚀 Typical Git Workflow

``` bash
git clone https://github.com/user/repo.git
cd repo

git checkout -b feature-branch

git add .
git commit -m "Feature added"

git push -u origin feature-branch

git pull origin main
git merge main
```

------------------------------------------------------------------------

#  Summary

This document covers core Git operations including:

-   Repository setup
-   Daily development workflow
-   Branch management
-   Remote repository interaction
-   Advanced Git techniques
-   GitHub CLI usage

Mastering these commands enables efficient collaboration and version
control in modern DevOps workflows.

