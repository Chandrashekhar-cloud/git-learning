# Day 1 — Git Core Commands

## What is Git

Git is a **version control system** that tracks changes in files over time.
It allows developers to:

* Save project history
* Collaborate with other developers
* Restore previous versions of files
* Track who made changes and when

Think of Git like a **super-powered save system** for code.

---

# How Git Works

```
YOUR LAPTOP                     GITHUB (Cloud)
===========                     ==============

Working Directory               Remote Repository
      |                                 |
   git add                          git push
      |                                 |
   Staging Area ----- git commit ----> Local Repository
```

### Git Areas

**Working Directory**

* The files you are currently editing.

**Staging Area**

* Files prepared to be committed using `git add`.

**Local Repository**

* Saved commit history on your laptop.

**Remote Repository**

* The repository stored on GitHub.

---

# Git Setup (One Time)

Check Git version

```
git --version
```

Configure username

```
git config --global user.name "Chandrashekhar"
```

Configure email

```
git config --global user.email "your@email.com"
```

Verify configuration

```
git config --list
```

Set default branch name

```
git config --global init.defaultBranch main
```

---

# Git Core Commands

## Initialize Repository

```
git init
```

Creates a new Git repository in the current directory.

---

## Clone Repository

```
git clone REPOSITORY_URL
```

Downloads an existing repository from GitHub to your local machine.

Example

```
git clone https://github.com/YOURUSERNAME/git-learning.git
```

---

## Check Repository Status

```
git status
```

Shows:

* Modified files
* Staged files
* Untracked files

---

## Add Files to Staging

Add specific file

```
git add filename
```

Add all files

```
git add .
```

---

## Commit Changes

```
git commit -m "message"
```

Saves staged changes to the local repository.

Example

```
git commit -m "Day 1: Add README file"
```

---

## Push to GitHub

```
git push
```

Uploads commits from your local repository to GitHub.

---

## Pull Changes

```
git pull
```

Downloads the latest changes from GitHub.

---

## View Commit History

```
git log
```

Shows full commit history.

Compact view

```
git log --oneline
```

---

# Additional Useful Commands

## See File Changes

```
git diff
```

Shows changes not yet staged.

---

## See Staged Changes

```
git diff --staged
```

Shows changes ready to be committed.

---

## View Commit Details

```
git show COMMIT_ID
```

Shows details of a specific commit.

---

## Check Connected Remote Repository

```
git remote -v
```

Shows which GitHub repository is connected.

---

# Commit Message Rules

Good commit messages are very important in real projects.

### Bad Examples

```
git commit -m "fix"
git commit -m "changes"
git commit -m "asdf"
```

### Good Examples

```
git commit -m "Add Dockerfile for Flask app"
git commit -m "Fix nginx port configuration"
git commit -m "Day 1: Linux navigation commands"
git commit -m "Add health check endpoint to API"
```

### Good Format

```
Verb + What you changed
```

Common verbs

* Add
* Fix
* Update
* Remove
* Refactor
* Create

---

# Day 1 Practice Summary

Tasks completed today:

* Created GitHub repository **git-learning**
* Cloned repository to local machine
* Created README.md file
* Added practice files
* Committed multiple changes
* Pushed commits to GitHub
* Viewed commit history

Minimum commits done: **5**

---

# Learning Goal

Goal: Become confident with Git fundamentals and daily developer workflow.

Next Steps:

* Git Branching
* Git Merge
* Pull Requests
* Team Collaboration
