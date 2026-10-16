# 13.2: Extra Practice

1. **Revert a merge:** merge a practice branch with `git merge --no-ff`, then undo it with `git revert -m 1 <merge hash>`. Read why a merge commit needs `-m` to say which parent to keep.
2. **Recover a deleted branch:** delete a branch with unmerged work using `git branch -D`, find its last commit in `git reflog` and bring it back with `git switch -c recovered <hash>`.
3. **Detached HEAD:** run `git switch --detach HEAD~2`, make a commit there, then keep it with `git switch -c kept-from-detached` before switching away.
4. **One file from the past:** restore a single file as it was two commits ago with `git restore --source=HEAD~2 <file>`, without moving the branch.
5. **ORIG_HEAD:** right after a reset or rebase I regret, try `git reset --hard ORIG_HEAD` as the quickest way back.
6. **Safer force pushes:** after amending a pushed commit on my own practice branch, push with `git push --force-with-lease --force-if-includes` rather than `--force`, then read what each flag protects against.
7. **When the reflog is not enough:** read what `git fsck --lost-found` finds and why `git gc` straight after a mistake can make recovery impossible.

## Questions to answer for myself

- Why does a reverted merge cause trouble when the same branch is merged again later?
- What does `--force-with-lease` check that `--force` does not?
- How long does the reflog keep an entry? Is it shared with anyone else who has cloned the repository?
