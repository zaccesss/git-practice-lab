# 15.2: Extra Practice

## Newer Git

1. **Config subcommands:** use `git config get user.email`, `git config set --global init.defaultBranch main` and `git config list --show-origin`. These replace the older flag style (`git config --get` and friends).
2. **Repository facts:** run `git repo info --all` to see what Git reports about this repository, such as its object format and reference format.
3. **Last change per file:** run `git last-modified` in this repository to see the commit that last touched each top-level path, the same thing GitHub shows beside each file in its file list.
4. **Comparing two versions of a branch:** after an interactive rebase, compare the old and new commits with `git range-diff main@{1}...HEAD`. The reflog hash of the branch before the rebase works in place of `main@{1}`.
5. **Background maintenance:** run `git maintenance start` in this repository, then `git config list --show-origin | grep maintenance` to see what it scheduled. Turn it off again with `git maintenance stop`.
6. **Partial clones:** clone a large public repository with `git clone --filter=blob:none`, then run `git backfill` to fetch the missing file contents in batches.
7. **Sparse checkout:** in that clone, run `git sparse-checkout set <folder>` so only one folder is on disk.
8. **Experimental replay:** read what `git replay` does differently from `git rebase` (it rewrites commits without touching the working directory) before trying it on a throwaway branch. It is marked experimental, so its options may still change.
9. **What is coming:** read Git's own list of planned breaking changes for Git 3.0, such as `main` as the default branch name for new repositories.

## GitHub releases and Actions

1. **Release attestations:** run `gh release verify` against a release from a repository that publishes attestations, then read what the check proves about where the release came from.
2. **Cancel superseded runs:** add a `concurrency` block with `cancel-in-progress: true` to the practice workflow from [module 08](../../08-github-actions), push twice quickly and check only the newer run finishes.
3. **Rerun only what failed:** make one job fail on purpose, fix it, then run `gh run rerun <run id> --failed` instead of rerunning the whole workflow.

## Questions to answer for myself

- Why did Git move `config` to subcommands when the old flags still work?
- What does a blobless clone save? What does `git backfill` do about the cost later?
- What would `concurrency` save on a repository that pays for its Actions minutes?
