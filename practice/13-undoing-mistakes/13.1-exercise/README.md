# 13.1: Exercise

## Which undo for which mistake

| The mistake | Already pushed? | The command |
| --- | --- | --- |
| Edited a file and want the last committed version back | No | `git restore <file>` |
| Staged a file by accident | No | `git restore --staged <file>` |
| Wrong message or a missed file in the last commit | No | `git add <file>` then `git commit --amend` |
| Last commit should not exist, but keep its changes staged | No | `git reset --soft HEAD~1` |
| Last commit should not exist, keep its changes unstaged | No | `git reset HEAD~1` (the default, `--mixed`) |
| Last commit and its changes should both go | No | `git reset --hard HEAD~1` |
| A commit is wrong and others may already have it | Yes | `git revert <hash>` |

## Steps

Work on a throwaway branch, `git switch -c practice/undo-demo`, so nothing here can touch `main`.

1. Edit a file, then throw the edit away with `git restore`. Edit it again, stage it, then unstage it with `git restore --staged` and confirm the edit is still in the file.
2. Commit with a deliberately bad message, then fix only the message with `git commit --amend`. Compare the hash before and after with `git log --oneline -1`.
3. Make three small commits. Undo the last one with each kind of reset in turn (`--soft`, then `--mixed`, then `--hard`), running `git status` after each to see where the changes ended up.
4. After the `--hard` reset, get the commit back: find it with `git reflog`, then `git reset --hard HEAD@{1}` (or the hash the reflog shows).
5. Push the branch, then undo one of its commits with `git revert <hash>` and look at the new commit it creates.
6. Delete the branch locally and on origin when done: `git switch main`, `git branch -D practice/undo-demo` then `git push origin --delete practice/undo-demo`.

## Questions to answer for myself

- Why is `git reset` on a pushed commit a problem for other people when it is harmless on my own machine?
- Where did the changes go after each of the three resets: staged, in the working directory or nowhere?
- Why does `git revert` add a commit instead of removing one?
