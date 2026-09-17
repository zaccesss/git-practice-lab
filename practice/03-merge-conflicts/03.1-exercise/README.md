# 03.1: Exercise

## Steps

1. On `main`, open [`conflict-practice.txt`](conflict-practice.txt) and change line 1 to anything I like. Commit it directly to `main`.
2. Create a branch from the commit before my change: `git checkout -b practice/conflict-demo HEAD~1`.
3. On this branch, change line 1 of the same file to something different. Commit it.
4. Switch back to `main` and run `git merge practice/conflict-demo`. Git will refuse to merge automatically and mark the file as conflicted.
5. Open the file. I will see conflict markers:

   ```text
   <<<<<<< HEAD
   my main branch version
   =======
   my branch version
   >>>>>>> practice/conflict-demo
   ```

6. Decide what the line should actually say, delete the markers and the version I am not keeping, then save the file.
7. Stage the resolved file: `git add practice/03-merge-conflicts/03.1-exercise/conflict-practice.txt`.
8. Finish the merge: `git commit` (Git pre-fills a merge commit message, I can keep it).
9. Run `git log --graph --oneline` and look at how the two branches rejoin.

## Questions to answer for myself

- Why did Git need my help here when it merges most changes automatically?
- What is the difference between `git merge --abort` and finishing the resolution?
- How would `git status` have told me a merge was in progress if I had walked away and come back?
