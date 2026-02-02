# Cats

Small practice repository used to learn Git and GitHub basics.

## What this repo is for

This repo is not a real project. It is a sandbox that I used to understand:

- How to create a Git repository
- How to track files with `git add` and `git commit`
- How to create and merge branches
- How to connect a local repo to GitHub and push changes

## Git workflow practised

Commands used in this repo include:

- `git init` to start a new repository in the `Cats` folder
- `git status` to check which files are untracked or modified
- `git add` to stage changes
- `git commit` to save a snapshot of the staged changes
- `git branch` and `git checkout` to create and switch branches
- `git merge` to bring changes from a feature branch back into the main branch
- `git remote add origin` and `git push -u origin main` to send the repo to GitHub

## File

- `cats.txt` simple text file that I edited several times to see how Git tracks changes over time

README.md

# Cats — Git Training Repository

This repository was created to practice essential Git and GitHub commands including:

- Initialising a repo
- Adding and committing files
- Creating and merging branches
- Viewing log history
- Connecting to a remote GitHub repository
- Pushing changes to `main`

## Skills Practised

| Concept               | Status          |
| --------------------- | --------------- |
| git init              | ✔ Learned       |
| git add / commit      | ✔ Practised     |
| git branch / checkout | ✔ Completed     |
| git merge             | ✔ Completed     |
| git push / pull       | ✔ Working fully |

## File Included

`cats.txt` — updated multiple times to test version control.

## Next Steps

- Create more branches and merge changes
- Try rebasing and resolving merge conflicts
- Start a real project repo using this workflow

# 🐱 Cats - Git Training Repository + Learning Notes

This repository began as a practical exercise in learning Git and GitHub using a simple file `cats.txt`. It is now a reference guide for understanding Git, tracking changes, branching, merging, and pushing to GitHub. This README contains all my Git notes so I can always return here when I need a reminder.

---

## 🔥 What this repository is for

- Practice using Git commands
- Learn how commits and branches work
- Understand how to connect local Git to GitHub
- Store notes for future reference
- Experiment safely without worrying about breaking anything

Main file used for testing: `cats.txt`

---

## 🧠 Git in Simple Terms

Git = a **time machine** for projects.

- Every save is a snapshot (**commit**)
- Git remembers every version
- You can return to old versions anytime
- You can work on different versions using **branches**
- You merge branches back together when finished
  Git does not auto-save - **you choose what to record**

---

## 📌 Core Git Workflow (Important!)

```
git status        # Check what changed
git add <file>    # Stage changes
git commit -m ""  # Save snapshot
git push          # Upload to GitHub
git pull          # Download changes from GitHub
```

Once I know this cycle, I can already use Git like a developer.

---

## 🏁 Commands I Used While Building This Repo

### 1. Git Configuration

```
git config --global user.name "z******s"
git config --global user.email "******.******@gmail.com"
git config --global user.name      # verify
git config --global user.email     # verify
```

### 2. Create Repo & Track Files

```
git init
git status
git add cats.txt
git commit -m "First commit: added cats.txt"
```

### 3. View Commit History

```
git log
git log --oneline
git log --oneline --graph
```

### 4. Branching + Merging

```
git branch test-branch
git checkout test-branch
# edit file + commit inside branch
git commit -m "Added branch-specific line"
git checkout main
git merge test-branch
# remove branch if finished
git branch -d test-branch
```

### 5. Connect to GitHub + Push

```
git remote add origin https://github.com/z***e**s/cats.git
git remote -v
git branch -M main
git push -u origin main
git push
```

---

## 🧩 Branch Concepts (Easy Understanding)

| Branch              | Purpose                 |
| ------------------- | ----------------------- |
| main                | stable version          |
| feature/test-branch | development/experiments |

Flow:

```
git branch new-idea
git checkout new-idea
# work + commit
git checkout main
git merge new-idea
git branch -d new-idea   # optional
```

---

## 🛠 Troubleshooting Quick Fixes

| Problem                                   | Cause                   | Fix                                      |
| ----------------------------------------- | ----------------------- | ---------------------------------------- |
| not a git repository                      | Git not initialized     | run `git init` or `cd` into repo         |
| repository not found                      | wrong remote URL        | `git remote set-url origin <url>`        |
| changes not appearing locally             | local repo outdated     | `git pull`                               |
| VS Code sees changes but terminal doesn't | different branch active | check `git branch` + VS Code bottom-left |

---

## 🚀 VS Code Workflow (GUI Version of Git)

1. Open folder in VS Code
2. Click **Source Control**
3. File appears under **CHANGES**
4. Stage using `+`
5. Write commit message → press **Ctrl + Enter**
6. Click Sync/Push icon to upload to GitHub
   VS Code = Git commands but with buttons.

---

## 📚 Git Cheat Sheet (Instant Memory Reload)

```
# setup
git config --global user.name "Name"
git config --global user.email "Email"

# workflow
git status
git add .
git commit -m "message"
git push
git pull

# branches
git branch
git branch new
git checkout new
git merge new

# github connection
git remote add origin <url>
git push -u origin main
```

---

## 📍 Next Skill Progression

- Create more branches & merge them
- Cause merge conflict on purpose + solve
- Try `git rebase`
- Clone repos using `git clone <url>`
- Start a real C / Python / Arduino/ Security repo

---

### ✔ Final Note

This README exists so I never forget my Git fundamentals.  
If I ever get stuck - **return here.**

Setup check: Git configured correctly on laptop.
