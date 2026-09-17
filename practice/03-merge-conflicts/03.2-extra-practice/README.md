# 03.2: Extra Practice

1. Cause a conflict on purpose, then abort it instead of resolving it: `git merge --abort`. Confirm `main` is back exactly where it started, as if the merge never happened.
2. Cause a conflict during a rebase instead of a merge (`git rebase main` while on a branch that touches the same line). Notice the resolution steps are similar, but the commands to continue differ: `git add` then `git rebase --continue`, not `git commit`.
3. Set up a three-way conflict: branch from `main`, let a teammate (a second branch) change the same line differently, then let a third branch also touch it. Merge all three back into `main` one at a time and resolve each conflict as it comes up.
4. Use `git diff` while a conflict is unresolved and read what it shows for a conflicted file, it looks different from a normal diff.
5. Configure a merge tool (`git config merge.tool <tool>`) if I have a GUI diff tool installed, then trigger a conflict and resolve it with `git mergetool` instead of editing markers by hand.

## Questions to answer for myself

- Why does `git rebase --continue` exist as a separate command from `git commit`, when both finish a conflict resolution?
- What state is my repository actually in while a conflict is unresolved, is it mid-merge, mid-commit or something else?
- When would I choose `git merge --abort` over just resolving the conflict?
