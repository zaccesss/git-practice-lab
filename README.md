# Git Practice Lab

Git Practice Lab is a small learning repository for practising Git, GitHub, and professional development workflow habits.

The repository started with a simple `cats.txt` file and now acts as a personal reference for version control basics, branch workflow, pull requests, and clean project history.

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

| Area                             | Status      |
| -------------------------------- | ----------- |
| Create a local Git repository    | Learned     |
| Track files with `git add`       | Practised   |
| Save snapshots with `git commit` | Practised   |
| View commit history              | Practised   |
| Create and switch branches       | Completed   |
| Merge a branch into `main`       | Completed   |
| Connect local Git to GitHub      | Completed   |
| Push and pull changes            | Working     |
| Use issues before coding         | In progress |
| Open pull requests               | In progress |
| Review pull request diffs        | In progress |

## Repository Files

| File              | Purpose                                                                             |
| ----------------- | ----------------------------------------------------------------------------------- |
| `cats.txt`        | Simple practice file used to test commits, branches, and merges.                    |
| `README.md`       | Main project overview and Git learning notes.                                       |
| `CONTRIBUTING.md` | Professional GitHub workflow guide for issues, branches, PRs, reviews, and cleanup. |

## Basic Git Workflow

Use this loop for normal local changes:

```powershell
git status
git add .
git commit -m "Describe what changed"
git push
git pull
```

What each command does:

| Command                   | Purpose                                                    |
| ------------------------- | ---------------------------------------------------------- |
| `git status`              | Shows changed, staged, and untracked files.                |
| `git add .`               | Stages changes ready for commit.                           |
| `git commit -m "message"` | Saves a snapshot of staged changes.                        |
| `git push`                | Uploads local commits to GitHub.                           |
| `git pull`                | Downloads and merges remote changes into the local branch. |

## Branch Workflow

Use branches when working on a feature, fix, documentation update, or practice task.

```powershell
git checkout main
git pull
git checkout -b feature/example-work

# Make changes.

git status
git add .
git commit -m "Add example work"
git push origin feature/example-work
```

After the branch is pushed, open a pull request on GitHub.

## Professional GitHub Workflow

For meaningful changes, use this full workflow:

```text
issue -> branch -> commit -> push -> pull request -> review -> merge -> cleanup
```

This creates a clear record of:

- What work was planned.
- Which branch contained the change.
- Which commits implemented it.
- Which pull request reviewed and merged it.
- Which issue was closed by the work.

The detailed workflow lives in [CONTRIBUTING.md](CONTRIBUTING.md).

## Branch Naming

Use clear branch names that describe the type of work.

| Type           | Branch format             | Example                         |
| -------------- | ------------------------- | ------------------------------- |
| Feature        | `feature/name-of-feature` | `feature/telemetry-dashboard`   |
| Bug fix        | `fix/name-of-bug`         | `fix/auth-validation`           |
| Documentation  | `docs/name-of-update`     | `docs/readme-cleanup`           |
| Refactor       | `refactor/name-of-change` | `refactor/config-loader`        |
| Coding problem | `solve/problem-name`      | `solve/top-k-frequent-elements` |

If Git cannot create a branch with a slash because of a local ref conflict, use a hyphenated name instead:

```powershell
git checkout -b docs-readme-cleanup
```

## Commit Message Examples

Good commit messages are short, specific, and written in the present tense.

```text
Add professional GitHub workflow guide
Clean up README structure
Fix branch workflow example
Document pull request cleanup steps
Solve LeetCode 347 with hash map approach
```

Avoid vague messages such as:

```text
update
fix stuff
changes
final
```

## Repo Name

The current local folder is still named `cats`, but the project is really about Git practice.

Recommended GitHub repository name:

```text
git-practice-lab
```

Other possible names:

- `git-training-sandbox`
- `github-learning-notes`
- `version-control-practice`
- `git-fundamentals-lab`

`git-practice-lab` is the best option because it is short, clear, and accurately describes the purpose of the repo.

## Suggested Next Steps

1. Rename the GitHub repository from `cats` to `git-practice-lab`.
2. Use issues and pull requests for all meaningful future changes.
3. Practise resolving a merge conflict on purpose.
4. Try `git clone`, `git rebase`, and pull request reviews.
5. Add a `.gitignore` file when the repo starts containing real code.
6. Start a separate real project repo for Python, C, Arduino, cybersecurity, or web development work.

## Current Practice Change

Last updated: May 2, 2026.

This documentation cleanup is being handled through the new workflow:

```text
Issue: #4 Add professional GitHub workflow guide
Pull request: #5 Add professional GitHub workflow guide
Branch: docs-professional-github-workflow
```

After merging the PR:

```powershell
git checkout main
git pull
git branch -d docs-professional-github-workflow
```


## Contact and Support

Open an [issue](https://github.com/zaccessss/git-practice-lab/issues) in this repository for questions or bugs.

You can also reach me directly at [code@isaacadjei.me](mailto:code@isaacadjei.me) or via my [website contact page](https://isaacadjei.me/contact).

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&height=80&section=footer" />
</p>