# Changelog

All notable changes to this project are documented here.
Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

---

## [Unreleased]

### Added

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

- The README's Contact section now links out to `SUPPORT.md` and `SECURITY.md` as callouts instead of plain prose
- The Repository Files table now spells licence as a noun in UK English
- The README rewritten in first person throughout, with a learning progress table and a proper index into the new practice modules
- Top badges added for the markdown lint workflow and the licence
- The README's detailed command tables moved to `docs/`, keeping the root file short
- `cats.txt` moved from the repository root into `practice/00-cats-original`
- `CONTRIBUTING.md`'s example commit messages and project-type sections now name their commit prefix explicitly
