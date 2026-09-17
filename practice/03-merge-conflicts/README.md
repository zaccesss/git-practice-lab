# 03: Merge Conflicts

I use this module to cause a real merge conflict on purpose, then resolve it properly, so I do not panic the first time it happens for real.

## Exercise

1. On `main`, open [`conflict-practice.txt`](conflict-practice.txt) and change line 1 to anything you like. Commit it directly to `main`.
2. Create a branch from the commit before your change: `git checkout -b practice/conflict-demo HEAD~1`.
3. On this branch, change line 1 of the same file to something different. Commit it.
4. Switch back to `main` and run `git merge practice/conflict-demo`. Git will refuse to merge automatically and mark the file as conflicted.
5. Open the file. You will see conflict markers:

   ```text
   <<<<<<< HEAD
   your main branch version
   =======
   your branch version
   >>>>>>> practice/conflict-demo
   ```

6. Decide what the line should actually say, delete the markers and the version you are not keeping, then save the file.
7. Stage the resolved file: `git add practice/03-merge-conflicts/conflict-practice.txt`.
8. Finish the merge: `git commit` (Git pre-fills a merge commit message, you can keep it).
9. Run `git log --graph --oneline` and look at how the two branches rejoin.

## Questions to answer for yourself

- Why did Git need your help here when it merges most changes automatically?
- What is the difference between `git merge --abort` and finishing the resolution?
- How would `git status` have told you a merge was in progress if you had walked away and come back?

## Why this matters to me

A merge conflict is not an error, it is Git correctly refusing to guess when two people changed the same thing. I will hit this in real projects regardless, the only difference practice makes is not being afraid of it.
