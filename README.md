# Git Practice Lab

[![Markdown Lint](https://github.com/zaccesss/git-practice-lab/actions/workflows/markdownlint.yml/badge.svg)](https://github.com/zaccesss/git-practice-lab/actions/workflows/markdownlint.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

I use this repository to practise Git, GitHub and the professional workflow habits I want to be automatic before I rely on them in a real project. It started with a single `cats.txt` file to test my first commits and branches. It has since grown into a structured set of practice modules I come back to whenever I want to drill something specific or try a GitHub feature I have not used before.

## Practice modules

The real content lives in [practice/](practice), ten modules covering everything from staging a file for the first time through to the real aliases I use daily. Each module is split into an exercise, extra practice and a self-test. See [practice/README.md](practice/README.md) for the full list.

## Documentation

Detailed reference lives in [docs/](docs) rather than cluttering this file:

| Doc | What it covers |
| --- | --- |
| [docs/glossary.md](docs/glossary.md) | Every Git and GitHub term used across the modules, defined plainly |
| [docs/command-reference.md](docs/command-reference.md) | Every command in this repository, explained in full |
| [docs/github-ui-vs-terminal.md](docs/github-ui-vs-terminal.md) | The same task shown both through the GitHub web UI and the terminal |

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
| My real daily aliases end to end | In progress |

I update this table as I actually work through each module, not in advance.

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

Commit subjects follow the same conventional prefixes I use across all my other repositories, short, specific and in the imperative:

| Prefix | Use for | Example |
| --- | --- | --- |
| `feat:` | A new feature or module | `feat: add nine hands-on practice modules` |
| `fix:` | Correcting something wrong | `fix: correct the rebase step order in 04.1` |
| `docs:` | Documentation-only changes | `docs: add the command reference` |
| `chore:` | Housekeeping, config, no user-facing change | `chore: add issue template config` |
| `refactor:` | Restructuring without changing behaviour | `refactor: split modules into exercise, extra practice and self-test` |
| `test:` | Adding or correcting a self-test | `test: add a self-test to module 06` |
| `style:` | Formatting only, no content change | `style: fix a stray Oxford comma` |

The full step by step process, including opening issues, pushing branches, reviewing diffs and cleaning up after a merge, lives in [CONTRIBUTING.md](CONTRIBUTING.md).

## What is next for me

- Work through the remaining practice modules, in particular the GitHub Actions and remote collaboration ones.
- Add a module on GitHub Projects once I actually use one for something real.
- Keep [09-advanced](practice/09-advanced) updated as GitHub ships new features worth trying.
- Follow up in `dotfiles` on the alias gaps found in [practice/10-daily-workflow-and-aliases](practice/10-daily-workflow-and-aliases).

## Contact and support

Open an [issue](https://github.com/zaccesss/git-practice-lab/issues) in this repository for questions or bugs. See [SUPPORT.md](SUPPORT.md) for the full breakdown of where to go.

> [!TIP]
> Reach me directly at [code@isaacadjei.me](mailto:code@isaacadjei.me) or through the [website contact page](https://isaacadjei.me/contact).

> [!IMPORTANT]
> For a security issue, follow [SECURITY.md](SECURITY.md) rather than posting publicly.
