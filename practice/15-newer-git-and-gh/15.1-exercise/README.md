# 15.1: Exercise

## Newer `gh` commands

| What I am doing | Command |
| --- | --- |
| Create a branch linked to an issue, so the issue shows it under Development | `gh issue develop <issue> --checkout` |
| Open an issue as a sub-issue of another | `gh issue create --parent <issue>` |
| Watch a pull request's checks until they finish | `gh pr checks --watch` |
| Show only the checks that are required to merge | `gh pr checks --required` |
| Bring a pull request branch up to date with its base | `gh pr update-branch` (add `--rebase` to rebase instead of merging) |
| Open a pull request that reverts a merged one | `gh pr revert <number>` |
| See every rule that would apply to a branch name | `gh ruleset check <branch>` |
| List the rulesets on a repository | `gh ruleset list` |
| Open the current repository, file or pull request in the browser | `gh browse` |

## Steps

1. Open an issue for a small change, then run `gh issue develop <issue> --checkout`. Open the issue in the browser and find the branch in its **Development** section.
2. Open a second issue as a child of the first with `gh issue create --parent <issue>` and look at the parent's progress.
3. Make the change, push and open the pull request. Run `gh pr checks --watch` and let it report when the lint check finishes.
4. Merge something else to `main` first so my branch falls behind, then run `gh pr update-branch` and check the branch picked up the new commit.
5. Merge the pull request, then undo it with `gh pr revert <number>`. Read the revert pull request it opens, then close it without merging.
6. Run `gh ruleset check main` and `gh ruleset check practice/anything` to compare which rules each branch name would meet.

## Questions to answer for myself

- What does `gh issue develop` give me that `git switch -c` alone does not?
- Why does `gh pr revert` open a new pull request instead of pushing a revert straight to `main`?
- When would `gh pr update-branch --rebase` be the wrong choice?
