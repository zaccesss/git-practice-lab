# 07: GitHub Features

I use this module to practise the parts of GitHub that live outside plain Git: issues, pull requests, releases and the project-management tools built on top of them.

## Exercise

1. Open an issue on this repository using one of the two YAML forms in [.github/ISSUE_TEMPLATE](../../.github/ISSUE_TEMPLATE). Notice how the structured fields differ from a blank text box.
2. Create a branch named after that issue, make a small change, push it and open a pull request that references `closes #<issue number>`.
3. Add a label to the issue and the pull request from the repository's real label set (I always run `gh label list` first rather than guessing a name that might not exist).
4. Once the pull request is merged, confirm the issue closed automatically, then check that the branch was deleted and its remote-tracking ref pruned (`git fetch --prune`).
5. Create a tag on a commit that matters to me: `git tag -a v0.1.0 -m "First practice milestone"`, then push it: `git push origin v0.1.0`.
6. On GitHub, turn that tag into a release with a short description of what it marks.
7. Look at the repository's Insights tab and the Actions tab, even with nothing to see yet, so I know where to look once there is.

## Questions to answer for myself

- What is the actual mechanism that closes an issue automatically? Why does the keyword have to be in the pull request description rather than a commit message?
- What is the difference between a Git tag and a GitHub release?
- When would I reach for GitHub Discussions instead of an issue?

## Why this matters to me

The issue-to-merge cycle I use across every one of my own repositories only works because I understand what each GitHub feature is actually doing underneath, not just which buttons to click.
