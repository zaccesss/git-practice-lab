# 01.2: Extra Practice

Harder variations once the [01.1 exercise](../01.1-exercise) feels automatic.

1. Stage a file, then edit it again before committing. Run `git diff` (unstaged) and `git diff --staged` (staged) side by side and notice they show two different things.
2. Unstage a file without losing the change: `git restore --staged notes.txt`. Confirm the edit is still on disk afterwards.
3. Throw away an uncommitted change entirely: `git restore notes.txt`. Confirm this one really does delete the edit, unlike the previous step.
4. Stage only part of a file's changes using `git add -p`, walking through each hunk and choosing yes or no. Commit just the staged hunk, then check the rest is still sitting unstaged.
5. Write a commit, then look at exactly what it changed with `git show <hash>`, without touching `git log` at all.
6. Rename a file with `git mv old.txt new.txt` instead of deleting and recreating it, then check `git status` reports it as a rename, not a delete plus an add.

## Questions to answer for myself

- Why does Git treat a rename as a rename only sometimes, what threshold decides that?
- What is the actual difference between `git restore` and `git restore --staged`? Why does the flag matter so much?
- When would partial staging with `git add -p` be the right call instead of committing a whole file's changes at once?
