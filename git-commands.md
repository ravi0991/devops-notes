#  Git Basic Commands Guide

This document covers essential Git commands grouped by category:

-   Setup & Configuration
-   Workflow
-   Viewing Changes

------------------------------------------------------------------------

# 1️⃣ Setup & Configuration

##  git config

**Purpose:** Configure username and email for Git.

### Set Global Username & Email

``` bash
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"
```

### Verify Configuration

``` bash
git config --list
```

------------------------------------------------------------------------

##  git init

**Purpose:** Initialize a new Git repository.

``` bash
git init
```

------------------------------------------------------------------------

# 2️⃣ Workflow

##  git status

**Purpose:** Check the current state of files (tracked, modified,
staged, untracked).

``` bash
git status
```

------------------------------------------------------------------------

##  git add

**Purpose:** Add files to the staging area.

### Add Single File

``` bash
git add filename.txt
```

### Add All Files

``` bash
git add .
```

------------------------------------------------------------------------

##  git commit

**Purpose:** Save staged changes to the local repository.

``` bash
git commit -m "Your commit message here"
```

Example:

``` bash
git commit -m "Initial commit"
```

------------------------------------------------------------------------

# 3️⃣ Viewing Changes

##  git log

**Purpose:** View detailed commit history.

``` bash
git log
```

------------------------------------------------------------------------

##  git log --oneline

**Purpose:** View commit history in compact single-line format.

``` bash
git log --oneline
```

Example Output:

    a3f5d2b Added README file
    b7c9e1a Initial commit

------------------------------------------------------------------------

#  Basic Workflow Example

``` bash
git init
git status
git add .
git commit -m "Initial commit"
git log --oneline
```

------------------------------------------------------------------------

# 4️⃣ Remote Repository

## git remote

**Purpose:** Manage remote repositories connected to your local
repository.

### View Remote Repositories

``` bash
git remote -v
```

### Add Remote Repository

``` bash
git remote add origin https://github.com/username/repository.git
```

### Update Remote URL

``` bash
git remote set-url origin https://github.com/username/new-repository.git
```

------------------------------------------------------------------------

# 5️⃣ Branching

## git branch

**Purpose:** List or create branches.

List branches:

``` bash
git branch
```

Create new branch:

``` bash
git branch feature-branch
```

------------------------------------------------------------------------

## git checkout

**Purpose:** Switch between branches.

``` bash
git checkout feature-branch
```

Create and switch to new branch:

``` bash
git checkout -b feature-branch
```

------------------------------------------------------------------------

## git merge

**Purpose:** Merge one branch into another.

``` bash
git merge feature-branch
```

------------------------------------------------------------------------

## Delete Branch

Delete local branch (safe):

``` bash
git branch -d feature-branch
```

Force delete local branch:

``` bash
git branch -D feature-branch
```

Delete remote branch:

``` bash
git push origin --delete feature-branch
```

------------------------------------------------------------------------

# 6️⃣ Remote Synchronization

##  git push

**Purpose:** Push local commits to a remote repository.

``` bash
git push origin main
```

### Push New Branch

``` bash
git push -u origin feature-branch
```

------------------------------------------------------------------------

##  git pull

**Purpose:** Fetch and merge changes from a remote repository.

``` bash
git pull origin main
```

------------------------------------------------------------------------

#  Basic Workflow Example

``` bash
git init
git remote add origin https://github.com/username/repository.git
git status
git add .
git commit -m "Initial commit"
git branch feature-branch
git checkout feature-branch
git push -u origin feature-branch
git pull origin main
git log --oneline
```

added a new code to dev branch
this code is in progress
login feature code added
this is a good feature which will fix all the bugs in application
new code
login feature code added
this is a good feature which will fix all the bugs in application
login feature code added
this is a good feature which will fix all the bugs in application
