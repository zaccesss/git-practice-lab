# 01.1: Exercise

## Steps

1. Create a new file called `notes.txt` in this folder with one line of text.
2. Run `git status` and read what it says about the new file.
3. Stage it with `git add practice/01-basics/01.1-exercise/notes.txt`.
4. Run `git status` again and notice the file has moved from "untracked" to "changes to be committed".
5. Commit it: `git commit -m "Add practice notes file"`.
6. Change the line in `notes.txt`, then run `git diff` before staging, to see the unstaged change.
7. Stage and commit the change.
8. Run `git log --oneline` and count how many commits I have made in this folder.

## Questions to answer for myself

- What is the difference between the working directory, the staging area and the last commit?
- What does `git diff` show that `git status` does not?
- What happens if I run `git add .` from the repository root instead of naming a specific file?
