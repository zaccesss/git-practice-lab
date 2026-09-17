# 07.1: Exercise

## Steps

1. Open an issue on this repository using one of the two YAML forms in [.github/ISSUE_TEMPLATE](../../../.github/ISSUE_TEMPLATE). Notice how the structured fields differ from a blank text box.
2. Drag an image (a screenshot works fine) into the issue body while writing it. Confirm GitHub uploads it and inserts the markdown automatically rather than me writing the image link by hand.
3. Create a branch named after that issue, make a small change, push it and open a pull request that references `closes #<issue number>`.
4. Add a label to the issue and the pull request from the repository's real label set (I always run `gh label list` first rather than guessing a name that might not exist).
5. Once the pull request is merged, confirm the issue closed automatically, then check that the branch was deleted and its remote-tracking ref pruned (`git fetch --prune`).
6. Create a tag on a commit that matters to me: `git tag -a v0.1.0 -m "First practice milestone"`, then push it: `git push origin v0.1.0`.
7. On GitHub, turn that tag into a release with a short description of what it marks.
8. Look at the repository's Insights tab and the Actions tab, even with nothing to see yet, so I know where to look once there is.

## Questions to answer for myself

- What is the actual mechanism that closes an issue automatically? Why does the keyword have to be in the pull request description rather than a commit message?
- Where does an image dragged into an issue or pull request actually get stored? Is it part of the repository?
- What is the difference between a Git tag and a GitHub release?
- When would I reach for GitHub Discussions instead of an issue?
