# 06.1: Exercise

## Steps

1. On GitHub, fork this repository into a second account or use a throwaway repository I own.
2. Clone my fork locally: `git clone <my fork's URL>`.
3. Add the original repository as a second remote: `git remote add upstream https://github.com/zaccesss/git-practice-lab.git`.
4. Run `git remote -v` and confirm I now have both `origin` (my fork) and `upstream` (the original) listed.
5. Create a branch, make a small change, push it to my fork: `git push origin my-branch-name`.
6. Open a pull request from my fork's branch into the original repository's `main`.
7. Separately, practise keeping my fork's `main` up to date: `git fetch upstream`, then `git merge upstream/main` while on my own `main`.

## Questions to answer for myself

- What is the actual difference between `origin` and `upstream` in this setup?
- Why does a pull request from a fork need both remotes configured, but a pull request from a branch on the same repository does not?
- What happens if I push to `origin main` on my fork without first syncing it with `upstream/main`?
