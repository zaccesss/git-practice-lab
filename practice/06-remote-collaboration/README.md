# 06: Remote Collaboration

I use this module to practise the fork, clone and pull request flow this repository actually uses, from the other side, as if I were an outside contributor.

## Exercise

1. On GitHub, fork this repository into a second account or use a throwaway repository you own.
2. Clone your fork locally: `git clone <your fork's URL>`.
3. Add the original repository as a second remote: `git remote add upstream https://github.com/zaccesss/git-practice-lab.git`.
4. Run `git remote -v` and confirm you now have both `origin` (your fork) and `upstream` (the original) listed.
5. Create a branch, make a small change, push it to your fork: `git push origin your-branch-name`.
6. Open a pull request from your fork's branch into the original repository's `main`.
7. Separately, practise keeping your fork's `main` up to date: `git fetch upstream`, then `git merge upstream/main` while on your own `main`.

## Questions to answer for yourself

- What is the actual difference between `origin` and `upstream` in this setup?
- Why does a pull request from a fork need both remotes configured, but a pull request from a branch on the same repository does not?
- What happens if you push to `origin main` on your fork without first syncing it with `upstream/main`?

## Why this matters to me

Every open source contribution I might make starts here. [CONTRIBUTING.md](../../CONTRIBUTING.md) describes the branch-based workflow I use inside this repository, this module practises the fork-based version I need when I do not have write access to a repository at all.
