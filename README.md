# Git Practice Lab

Git Practice Lab is a small learning repository for practising Git, GitHub and professional development workflow habits.

The repository started with a simple `cats.txt` file and now acts as a reference for version control basics, branch workflow, pull requests and clean project history.

## Purpose

This repo is not a production software project. It is a sandbox for learning how developers manage changes in a professional way.

It is used to practise:

- Creating and managing a local Git repository.
- Tracking file changes with `git add` and `git commit`.
- Reading project state with `git status` and `git log`.
- Creating branches for isolated work.
- Merging changes back into `main`.
- Connecting a local repository to GitHub.
- Using issues and pull requests to document work.
- Reviewing diffs before merging.

## Current Learning Progress

| Area                              | Status    |
| ---------------------------------- | --------- |
| Create a local Git repository      | Completed |
| Track files with `git add`         | Practised |
| Save snapshots with `git commit`   | Practised |
| View commit history                | Practised |
| Create and switch branches         | Completed |
| Merge a branch into `main`         | Completed |
| Connect local Git to GitHub        | Completed |
| Push and pull changes              | Practised |
| Use issues before coding           | Practised |
| Open pull requests                 | Practised |
| Review pull request diffs          | Practised |

## Repository Files

| File              | Purpose                                                                      |
| ----------------- | ------------------------------------------------------------------------------ |
| `cats.txt`        | Simple practice file used to test commits, branches and merges.                |
| `README.md`       | Project overview and Git learning notes.                                       |
| `CONTRIBUTING.md` | Full workflow guide for issues, branches, pull requests, reviews and cleanup.  |
| `LICENSE`         | MIT license for the repository.                                                |

## Basic Git Workflow

The everyday loop for local changes:

```powershell
git status
git add .
git commit -m "Describe what changed"
git push
git pull
```

| Command                   | Purpose                                                     |
| -------------------------- | ------------------------------------------------------------ |
| `git status`               | Shows changed, staged and untracked files.                   |
| `git add .`                | Stages changes ready for commit.                              |
| `git commit -m "message"`  | Saves a snapshot of staged changes.                           |
| `git push`                 | Uploads local commits to GitHub.                              |
| `git pull`                 | Downloads and merges remote changes into the local branch.   |

## Branch and Pull Request Workflow

For meaningful changes, this repo follows:

```text
issue -> branch -> commit -> push -> pull request -> review -> merge -> cleanup
```

Branches use a prefix that describes the type of work:

| Type           | Branch format             | Example                         |
| --------------- | -------------------------- | --------------------------------- |
| Feature         | `feature/name-of-feature`  | `feature/telemetry-dashboard`     |
| Bug fix         | `fix/name-of-bug`          | `fix/auth-validation`             |
| Documentation   | `docs/name-of-update`      | `docs/readme-cleanup`             |
| Refactor        | `refactor/name-of-change`  | `refactor/config-loader`          |
| Coding problem  | `solve/problem-name`       | `solve/top-k-frequent-elements`   |

If Git cannot create a branch with a slash because of a local ref conflict, use a hyphenated name instead, for example `git checkout -b docs-readme-cleanup`.

Good commit messages are short, specific and written in the present tense, for example `Fix branch workflow example` rather than `update` or `fix stuff`.

The full step by step process, including opening issues, pushing branches, reviewing diffs and cleaning up after a merge, lives in [CONTRIBUTING.md](CONTRIBUTING.md).

## Suggested Next Steps

1. Use issues and pull requests for all meaningful future changes.
2. Practise resolving a merge conflict on purpose.
3. Try `git clone`, `git rebase` and pull request reviews.
4. Add a `.gitignore` file when the repo starts containing real code.
5. Start a separate project repo for Python, C, Arduino, cybersecurity or web development work.

## Contact

Open an [issue](https://github.com/zaccesss/git-practice-lab/issues) in this repository for questions or bugs.

Reach out directly at [code@isaacadjei.me](mailto:code@isaacadjei.me) or through the [website contact page](https://isaacadjei.me/contact).
