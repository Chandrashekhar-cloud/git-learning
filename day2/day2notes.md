# Git Day 02 - Branching + Merging + Pull Requests

## Theory — Why Branches?
- In real companies you NEVER commit directly to main branch
- You create a feature branch, work there, then merge through a Pull Request
- Someone reviews your code before it merges — this is professional workflow
```
main branch:    A --- B --- C --- F  (production code)
                             \
feature branch:               D --- E  (your new feature)

When feature is ready: merge D+E into main at point F
Main stays clean. Multiple people can work simultaneously.
```

---

## Branch Commands

| Command | What it does |
|---------|-------------|
| `git branch` | List all local branches |
| `git branch -a` | List all branches including remote |
| `git branch feature-login` | Create new branch |
| `git checkout feature-login` | Switch to branch |
| `git checkout -b feature-login` | Create AND switch in one command ⭐ |
| `git switch feature-login` | Modern way to switch branches |
| `git switch -c feature-login` | Modern way to create and switch |
| `git merge feature-login` | Merge feature-login INTO current branch |
| `git branch -d feature-login` | Delete branch after merging |
| `git branch -D feature-login` | Force delete branch |
| `git push origin feature-login` | Push branch to GitHub |
| `git pull origin main` | Pull latest main into current branch |
| `git log --all --oneline --graph` | Visual branch history |

---

## Pull Requests — Full Workflow ⭐

### Step 1: Create feature branch
```bash
git checkout -b feature-add-about-page
```

### Step 2: Make your changes
```bash
echo 'About page content' > about.md
git add .
git commit -m 'Add about page'
```

### Step 3: Push branch to GitHub
```bash
git push origin feature-add-about-page
```

### Step 4: Create PR on GitHub
- Go to github.com
- You will see **"Compare and pull request"** button
- Click it → Add title and description
- Click **"Create pull request"**

### Step 5: Review and Merge
- Click **"Merge pull request"** on GitHub

### Step 6: Pull merged changes back locally
```bash
git checkout main
git pull origin main
```

### Step 7: Delete feature branch
```bash
git branch -d feature-add-about-page
```

---

## Merge Conflicts — How to Fix

A conflict happens when 2 branches changed the same line.
Git cannot decide which version to keep.
```bash
# Git shows this inside the file:
<<<<<<< HEAD (your branch)
This is my version of the line
=======
This is the other branch version
>>>>>>> feature-branch
```

### Fix Steps:
```bash
# Step 1: Open the file and edit it
# Delete ALL the markers: <<<<<<< ======= >>>>>>>
# Keep only the version you want

# Step 2: Stage and commit
git add .
git commit -m "Resolve merge conflict"
git push
```

---

## Key Takeaways
- `git checkout -b branchname` — most used command for starting new work
- ALWAYS create a feature branch — never commit directly to main
- PR = Pull Request = asking to merge your branch into main after review
- `git pull origin main` after merging — keep your local main up to date
- `git branch -d` after merging — clean up old branches
- `git log --oneline --graph` — shows visual history of all branches
- Merge conflicts are NORMAL — just edit the file, remove markers, commit

---

## Full PR Workflow Summary
```
create branch → make commits → push branch →
open PR on GitHub → get reviewed → merge PR →
git pull origin main → delete old branch
```

---

## Git Commit
```bash
git add .
git commit -m "Day 2: branching merging and pull requests"
git push
```
