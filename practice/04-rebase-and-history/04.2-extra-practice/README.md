# 04.2: Extra Practice

1. Reorder two commits during an interactive rebase by moving their lines in the editor, rather than changing `pick` to anything. Confirm the resulting log shows them in the new order.
2. Split one commit into two: `git rebase -i` with `edit` on the target commit, then `git reset HEAD~1` once the rebase pauses there, then commit the change in two smaller pieces before running `git rebase --continue`.
3. Drop a commit entirely from history by deleting its line during an interactive rebase (or changing `pick` to `drop`). Confirm it is genuinely gone from `git log`, not just hidden.
4. Rebase a feature branch onto an updated `main` (`git checkout my-branch && git rebase main`) after `main` has moved on, instead of merging `main` into the branch. Compare the resulting history graph to what a merge would have produced.
5. Use `git commit --fixup <hash>` to mark a small correction as belonging to an earlier commit, then run `git rebase -i --autosquash` and watch Git reorder and squash it automatically.

## Questions to answer for myself

- Why does splitting a commit require `edit` rather than `squash` in the rebase todo list?
- What actually happens to the original commits after a rebase, are they deleted immediately?
- When would `--autosquash` save me real time over manually reordering a rebase todo list by hand?
