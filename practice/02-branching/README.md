# 02: Branching

I use this module to practise isolating work on a branch instead of committing everything straight to `main`.

## Exercise

1. Create a branch: `git checkout -b practice/branching-demo`.
2. Confirm you switched with `git branch` (the current branch has a `*` next to it).
3. Add a file called `branch-demo.txt` in this folder, commit it on this branch.
4. Switch back to `main`: `git checkout main`. Notice `branch-demo.txt` disappears from your working directory, it only exists on the other branch.
5. Merge the branch back in: `git merge practice/branching-demo`. Confirm `branch-demo.txt` is now on `main` too.
6. Delete the branch now it is merged: `git branch -d practice/branching-demo`.
7. Repeat the exercise, but this time try `git switch` and `git switch -c` instead of `git checkout`, the newer, more explicit commands for the same job.

## Questions to answer for yourself

- What actually moves when you switch branches, the commits or your working directory?
- Why does Git let you delete a branch with `-d` only after it is merged? What does `-D` do differently?
- What is `HEAD` pointing at while you are on a branch?

## Why this matters to me

Branching is what makes the issue-to-PR workflow I follow in [CONTRIBUTING.md](../../CONTRIBUTING.md) possible. I never commit anything meaningful straight to `main`, this is the isolation that makes reviewing and reverting my own work possible.
