# 05.1: Exercise

## Stash

1. Start editing a file in this folder without committing.
2. Try to switch to another branch, Git will complain if the change conflicts with that branch.
3. Instead, run `git stash` to shelve the change and clean my working directory.
4. Switch branches freely, then switch back.
5. Run `git stash pop` to bring the change back and remove it from the stash list.
6. Repeat, but this time use `git stash push -m "a description"` so `git stash list` is readable when I have more than one stash saved.

## Cherry-pick

1. Create a branch, make one small commit on it.
2. Switch to a different branch (not `main`, not the one I just committed on).
3. Run `git cherry-pick <the commit hash>` to copy that single commit onto my current branch, without merging the whole branch.
4. Run `git log --oneline` and confirm the commit now exists in two places with two different hashes, cherry-pick copies the change, it does not move it.

## Questions to answer for myself

- Why does `git stash` sometimes still cause a conflict when I pop it?
- When would cherry-picking a single commit be the right call instead of merging or rebasing a whole branch?
- What happens to the stash if I run `git stash drop` versus `git stash pop`?
