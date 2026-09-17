# 04.1: Exercise

## Steps

1. Make three small, separate commits in this folder (for example: create a file, add a line, fix a typo in that line).
2. Run `git log --oneline` and note the three commit hashes.
3. Run `git rebase -i HEAD~3` to open an interactive rebase for the last three commits.
4. In the editor that opens, change `pick` to `squash` (or `s`) on the second and third commits, keeping `pick` on the first. Save and close.
5. Git will open a second editor asking for the combined commit message. Write one message describing all three changes together, save and close.
6. Run `git log --oneline` again, the three commits are now one.
7. Practise amending a commit message without touching its content: `git commit --amend -m "A better message"`.
8. Separately, practise fixing a typo in the file I just committed without creating a new commit: edit the file, `git add` it, then `git commit --amend --no-edit`.

## Questions to answer for myself

- Why is rebasing safe on a branch only I am working on, but risky on a branch others have already pulled?
- What is the difference between `git rebase` and `git merge` when bringing `main` into a feature branch?
- What does `git reflog` show? How could it save me if an interactive rebase went wrong?
