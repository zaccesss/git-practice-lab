# 02.2: Extra Practice

1. Create two branches from `main` at the same time, `practice/branch-a` and `practice/branch-b`, each changing a different file. Merge both into `main` and confirm neither overwrote the other.
2. Try `git branch --merged` and `git branch --no-merged` on `main` to see which of my branches are safe to delete and which still have unmerged work.
3. Rename a branch I am currently on: `git branch -m better-name`. Confirm the old name is gone entirely, this is a rename, not a copy.
4. Create a branch, push it, then delete the local copy only: `git branch -d branch-name` after checking out something else. Confirm the branch still exists on GitHub with `git branch -r`.
5. Now delete it from GitHub too: `git push origin --delete branch-name`. Run `git fetch --prune` and confirm the remote-tracking reference disappears locally as well.
6. Compare `git log main..my-branch` (commits on my branch not yet on main) against `git log my-branch..main` (the reverse). Explain out loud what each one is actually showing.

## Questions to answer for myself

- Why is deleting a branch locally and deleting it on GitHub two separate steps rather than one?
- What does `git branch --no-merged` protect me from accidentally doing?
- What is the practical difference between a branch and a tag, given both are just a name pointing at a commit?
