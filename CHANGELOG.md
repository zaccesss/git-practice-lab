# Changelog

All notable changes to this project are documented here.
Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

---

## [Unreleased]

## [0.0.1] - 2026-10-22

### Added

- Five new practice modules, each with an exercise, extra practice and a self-test: 11 GitLab, 12 signing and security, 13 undoing mistakes, 14 planning with GitHub Projects and 15 newer Git and GitHub CLI commands
- `practice/11-gitlab/11.1-exercise/example-gitlab-ci.yml`, a two-stage pipeline to paste into a GitLab project
- GitLab terms plus the new Git and GitHub terms in the glossary, with matching sections in the command reference
- Rows in `docs/github-ui-vs-terminal.md` for issue branches, sub-issues, reverting and updating pull requests
- `CODEOWNERS`, `CODE_OF_CONDUCT.md`, `SECURITY.md` and `SUPPORT.md`, matching the rest of the fleet
- `.markdownlint.json` and a markdownlint CI workflow, with its own `.github/workflows/README.md`
- YAML issue forms for bug reports and enhancements plus a pull request template
- This changelog
- `.github/ISSUE_TEMPLATE/config.yml` disabling the blank issue option, pointing to the security policy and code@isaacadjei.me instead
- Ten practice modules under `practice/`, covering basics, branching, merge conflicts, rebase and history, stash and cherry-pick, remote collaboration, GitHub features, GitHub Actions, an advanced module I revisit as GitHub ships new features and my real daily aliases
- Each module split into an `.1-exercise`, a `.2-extra-practice` and a `.3-self-test`, each with its own `README.md`
- `practice/00-cats-original`, home for my original `cats.txt` practice file, moved out of the repository root
- `practice/README.md` indexing all ten modules
- A sample workflow file in `practice/08-github-actions` to copy and experiment with, not part of this repository's own CI
- `docs/glossary.md`, `docs/command-reference.md` and `docs/github-ui-vs-terminal.md`, moving detailed explanations out of the README
- A commit message prefix table in the README and `CONTRIBUTING.md`, matching the conventional commit style I use across the rest of my repositories

### Changed

- `actions/checkout` moved from v4.4.0 to v7.0.1 in the lint workflow and the module 08 example
- `markdownlint-cli2-action` pinned to a commit at v24.2.0
- `CONTRIBUTING.md` uses `git switch` throughout, with a practice-module example in place of the competitive programming one
- Tidied the contributor guide examples.
- The README's Contact section now links out to `SUPPORT.md` and `SECURITY.md` as callouts instead of plain prose
- The Repository Files table wording tidied
- The README rewritten, with a learning progress table and a proper index into the new practice modules
- Top badges added for the markdown lint workflow and the licence
- The README's detailed command tables moved to `docs/`, keeping the root file short
- `cats.txt` moved from the repository root into `practice/00-cats-original`
- `CONTRIBUTING.md`'s example commit messages and project-type sections now name their commit prefix explicitly

### Fixed

- `docs/github-ui-vs-terminal.md` no longer says rulesets can only be created in the browser
