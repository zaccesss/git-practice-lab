# 09: Advanced Git and Newer GitHub Features

I use this module for the tools I reach for less often, plus newer GitHub features I have not built real habits around yet. I revisit this one periodically and add to it as GitHub ships something new worth trying.

## Git exercises

- **Reflog:** delete a branch on purpose without merging it, then recover its last commit with `git reflog` and `git checkout -b recovered-branch <hash>`.
- **Bisect:** pick an old commit I know was working, introduce a deliberate bug in a later commit, then use `git bisect start`, `git bisect good` and `git bisect bad` to let Git binary-search for the exact commit that broke it.
- **Worktrees:** run `git worktree add ../git-practice-lab-second main` to check out a second branch into a second folder without cloning the repository twice, useful when I want to compare two branches side by side.
- **Hooks:** add a local `.git/hooks/pre-commit` script that blocks a commit containing the word `TODO`, then try to commit a file with that word in it.

## GitHub features worth trying as they mature

- **Rulesets:** GitHub's newer, more flexible replacement for classic branch protection rules. I set one up on a throwaway repository and compare it to the old branch protection settings.
- **Merge queue:** useful once a repository has several pull requests landing on `main` at once, I read how it batches and re-tests pull requests before merging so I understand it before I ever need it on a busier project.
- **Private vulnerability reporting:** GitHub's built-in flow for someone to report a security issue privately without emailing me directly. I compare it against the SECURITY.md-based process I already use across my own repositories.
- **Codespaces:** a full cloud dev environment tied to a repository. I try opening this repository in one and running through an earlier module entirely inside it.

## Why this matters to me

Git and GitHub keep adding capability. The fleet-wide hygiene bundle I apply across my own repositories should reflect what is actually current, not just what I learned first. This module is where I try something new before deciding whether it belongs in that bundle.
