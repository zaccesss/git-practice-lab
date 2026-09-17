# 05.2: Extra Practice

1. Stash changes in more than one file, then run `git stash show -p` on the most recent stash to preview exactly what it contains before popping it.
2. Stash only part of a file's changes with `git stash push -p`, choosing hunks the same way `git add -p` does.
3. Apply a stash without removing it from the list: `git stash apply`. Confirm `git stash list` still shows it afterwards, unlike `pop`.
4. Create two stashes, then apply the older one by index: `git stash apply stash@{1}`.
5. Cherry-pick a commit that touches multiple files, then cherry-pick a range of several commits at once with `git cherry-pick <hash1>^..<hash2>`.
6. Cherry-pick a commit that causes a conflict on purpose, resolve it, then finish with `git cherry-pick --continue` instead of a plain commit.

## Questions to answer for myself

- Why would I choose `git stash apply` over `git stash pop` even though pop is more common?
- What does the `^` in `<hash1>^..<hash2>` actually change about which commits get included?
- If a cherry-picked commit conflicts, is the fix I make part of the original commit or a new one?
