# 09.2: Extra Practice - Newer GitHub Features

I revisit this list periodically and add to it as GitHub ships something new worth trying. Private vulnerability reporting is covered in [07.2](../../07-github-features/07.2-extra-practice) instead, since it fits naturally alongside the rest of the issue and security workflow there.

1. **Rulesets:** GitHub's newer, more flexible replacement for classic branch protection rules. Set one up on a throwaway repository and compare it to the old branch protection settings.
2. **Merge queue:** useful once a repository has several pull requests landing on `main` at once. Read how it batches and re-tests pull requests before merging, so I understand it before I ever need it on a busier project.
3. **Codespaces:** a full cloud dev environment tied to a repository. Try opening this repository in one and running through an earlier module entirely inside it.
4. **Custom properties:** GitHub's newer per-repository metadata fields (separate from topics), useful for tagging repositories with structured data an org can filter on. Try adding one to a repository I own.
5. **Immutable releases:** newer protection that locks a release's assets and tag once published. Create a release on a throwaway repository, enable it and confirm I can no longer overwrite the asset.

## Questions to answer for myself

- What does a ruleset let me express that classic branch protection could not?
- Why would a merge queue re-test a pull request against a moving target instead of the state it was originally reviewed against?
- What is genuinely different about developing inside a Codespace versus just cloning locally, beyond not needing my own machine?
