# Git Practice Lab

[![Markdown Lint](https://github.com/zaccesss/git-practice-lab/actions/workflows/markdownlint.yml/badge.svg)](https://github.com/zaccesss/git-practice-lab/actions/workflows/markdownlint.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

I use this repository to practise Git, GitHub and the professional workflow habits I want to be automatic before I rely on them in a real project. It started with a single `cats.txt` file to test my first commits and branches. It has since grown into a structured set of practice modules I come back to whenever I want to drill something specific or try a GitHub feature I have not used before.

## Practice modules

The real content lives in [practice/](practice), nine modules covering everything from staging a file for the first time through to writing a CI workflow and trying newer GitHub features as they mature. See [practice/README.md](practice/README.md) for the full list and the order I worked through them in.

## Learning progress

| Area | Status |
| --- | --- |
| Local repository basics (status, add, commit, log, diff) | Completed |
| Branching and merging | Completed |
| Resolving a real merge conflict on purpose | Completed |
| Interactive rebase, squashing, amending | Completed |
| Stash and cherry-pick | Completed |
| Fork and upstream remote collaboration | In progress |
| Issues, labels, tags and releases | In progress |
| Writing a GitHub Actions workflow from scratch | In progress |
| Reflog, bisect, worktrees and hooks | Not started |
| Newer GitHub features (rulesets, merge queue, Codespaces) | Not started |

I update this table as I actually work through each module, not in advance.

## Repository files

| File | Purpose |
| --- | --- |
| `practice/` | Nine hands-on modules, each with its own exercise and notes |
| `cats.txt` | My original practice file from before the modules existed |
| `CONTRIBUTING.md` | The branch, issue and pull request workflow I follow for every change here |
| `SUPPORT.md` | Where to go for help or to report something wrong |
| `SECURITY.md` | How to report a security issue privately |
| `CHANGELOG.md` | What changed here and when |
| `LICENSE` | The MIT licence covering this repository |

## Everyday Git workflow

The loop I use for local changes:

```bash
git status
git add .
git commit -m "Describe what changed"
git push
git pull
```

| Command | Purpose |
| --- | --- |
| `git status` | Shows changed, staged and untracked files |
| `git add .` | Stages changes ready for commit |
| `git commit -m "message"` | Saves a snapshot of staged changes |
| `git push` | Uploads local commits to GitHub |
| `git pull` | Downloads and merges remote changes into the local branch |

## Branch and pull request workflow

For anything beyond a one-line fix, I follow:

```text
issue -> branch -> commit -> push -> pull request -> review -> merge -> cleanup
```

Branches use a prefix that describes the type of work:

| Type | Branch format | Example |
| --- | --- | --- |
| Feature | `feature/name-of-feature` | `feature/telemetry-dashboard` |
| Bug fix | `fix/name-of-bug` | `fix/auth-validation` |
| Documentation | `docs/name-of-update` | `docs/readme-cleanup` |
| Refactor | `refactor/name-of-change` | `refactor/config-loader` |

> [!TIP]
> If Git cannot create a branch with a slash because of a local ref conflict, I use a hyphenated name instead, for example `git checkout -b docs-readme-cleanup`.

I keep commit subjects short, specific and in the imperative, for example `Fix branch workflow example` rather than `update` or `fix stuff`.

The full step by step process, including opening issues, pushing branches, reviewing diffs and cleaning up after a merge, lives in [CONTRIBUTING.md](CONTRIBUTING.md).

## What is next for me

- Work through the remaining practice modules, in particular the GitHub Actions and remote collaboration ones.
- Add a module on GitHub Projects once I actually use one for something real.
- Keep [09-advanced](practice/09-advanced) updated as GitHub ships new features worth trying.

## Contact and support

Open an [issue](https://github.com/zaccesss/git-practice-lab/issues) in this repository for questions or bugs. See [SUPPORT.md](SUPPORT.md) for the full breakdown of where to go.

> [!TIP]
> Reach me directly at [code@isaacadjei.me](mailto:code@isaacadjei.me) or through the [website contact page](https://isaacadjei.me/contact).

> [!IMPORTANT]
> For a security issue, follow [SECURITY.md](SECURITY.md) rather than posting publicly.
