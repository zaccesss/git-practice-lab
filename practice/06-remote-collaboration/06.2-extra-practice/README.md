# 06.2: Extra Practice

1. Rebase my fork branch onto `upstream/main` instead of merging, to practise the cleaner-history version of keeping a fork current: `git fetch upstream`, then `git rebase upstream/main` while on my branch.
2. Configure a second remote push URL so `git push` on `origin` accidentally cannot push to `upstream`: `git remote set-url --push upstream no-push`. Confirm attempting to push to `upstream` now fails safely.
3. Practise a stacked pull request: branch `feature-part-1` from `main`, open a pull request. Branch `feature-part-2` from `feature-part-1` before it merges, open a second pull request targeting `feature-part-1` instead of `main`. Once the first merges, retarget the second pull request to `main` on GitHub.
4. Add a co-author to a commit by hand: `git commit -m "message" -m "Co-authored-by: Name <email>"`, then confirm GitHub credits both people on the commit.
5. Practise reviewing someone else's pull request locally instead of only on GitHub: `gh pr checkout <number>`, run the code, then leave a review from the terminal with `gh pr review`.

## Questions to answer for myself

- Why would I rebase my fork onto upstream instead of merging, given both keep me up to date?
- What real problem does a stacked pull request solve that a single large pull request does not?
- What is the security reason `upstream` should usually be fetch-only for a fork I do not maintain?
