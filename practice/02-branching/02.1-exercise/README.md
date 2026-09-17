# 02.1: Exercise

## Steps

1. Create a branch: `git checkout -b practice/branching-demo`.
2. Confirm I switched with `git branch` (the current branch has a `*` next to it).
3. Add a file called `branch-demo.txt` in this folder, commit it on this branch.
4. Switch back to `main`: `git checkout main`. Notice `branch-demo.txt` disappears from my working directory, it only exists on the other branch.
5. Merge the branch back in: `git merge practice/branching-demo`. Confirm `branch-demo.txt` is now on `main` too.
6. Delete the branch now it is merged: `git branch -d practice/branching-demo`.
7. Repeat the exercise, but this time try `git switch` and `git switch -c` instead of `git checkout`, the newer, more explicit commands for the same job.

## Questions to answer for myself

- What actually moves when I switch branches, the commits or my working directory?
- Why does Git let me delete a branch with `-d` only after it is merged? What does `-D` do differently?
- What is `HEAD` pointing at while I am on a branch?
