# Git / GitHub Terminal Commands (Linux)

## Assumptions
- Linux
- git >= 2.43.0
- GitHub account
- HTTPS (PAT, not password)

---

## Setup (Run Once)
git --version
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --global credential.helper store

NOTE:
- GitHub requires a **Personal Access Token (PAT)** instead of a password
- Username = GitHub username
- Password = PAT

---

## Create Local Repository
mkdir myproject
cd myproject
git init

---

## OR Clone Existing Repository
git clone https://github.com/USERNAME/REPO.git
cd REPO

---

## Connect Local Repo to GitHub (First Time Only)
git branch -M main
git remote add origin https://github.com/USERNAME/REPO.git

Verify:
git remote -v

---

## First Push (IMPORTANT)
git push -u origin main

SPECIAL NOTE:
- `-u` sets the upstream branch
- This is REQUIRED only once per branch
- Without this, `git push` will FAIL

---

## Daily Workflow (After First Push)
git status
git add .
git commit -m "commit message"
git pull
git push

WHY THIS WORKS:
- Remote already exists
- Upstream already set
- Branch already pushed once

---

## Branching
git checkout -b feature-x
git add .
git commit -m "feature work"
git push -u origin feature-x

After first push of branch:
git push

---

## Merge Branch
git checkout main
git pull
git merge feature-x
git push

---

## Undo / Fix
Unstage file:
git restore --staged file.txt

Discard changes:
git restore file.txt

Amend last commit:
git commit --amend

---

## Verification Commands
git status
git branch
git branch -vv
git log --oneline

---

## Common Failures
Auth failed:
- PAT expired → regenerate
- Used password instead of PAT

Push rejected:
git pull --rebase
git push

No upstream error:
git push -u origin <branch>

---

