# 09.1: Exercise

## Git tools I reach for less often

1. **Reflog:** delete a branch on purpose without merging it, then recover its last commit with `git reflog` and `git checkout -b recovered-branch <hash>`.
2. **Bisect:** pick an old commit I know was working, introduce a deliberate bug in a later commit, then use `git bisect start`, `git bisect good` and `git bisect bad` to let Git binary-search for the exact commit that broke it.
3. **Worktrees:** run `git worktree add ../git-practice-lab-second main` to check out a second branch into a second folder without cloning the repository twice, useful when I want to compare two branches side by side.
4. **Hooks:** add a local `.git/hooks/pre-commit` script that blocks a commit containing the word `TODO`, then try to commit a file with that word in it.

## Questions to answer for myself

- Why does `git reflog` keep a record even of commits no branch points at any more?
- How does `git bisect` decide which commit to test next, is it a linear search or something smarter?
- What is the practical difference between a worktree and just cloning the repository a second time?
