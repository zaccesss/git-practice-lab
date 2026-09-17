# 08: GitHub Actions

I use this module to practise writing a CI workflow from scratch, rather than only ever copying one that already works.

## Exercise

1. Read [example-workflow.yml](example-workflow.yml) in this folder before copying anything, so I understand each section rather than treating it as a black box.
2. Copy it into `.github/workflows/practice.yml` on a branch of my own (never on `main` directly).
3. Push the branch and open a pull request. Watch the workflow run in the Actions tab and read its logs, not just its pass or fail status.
4. Change the `run` step to something that deliberately fails (for example `exit 1`), push again and watch the check turn red on the pull request.
5. Fix it, push again and watch it turn green.
6. Once I am comfortable, delete `.github/workflows/practice.yml` again, this file is for practice, not for this repository's real CI.
7. Try adding a second job that only runs if the first one succeeds, using `needs:`.

## Questions to answer for myself

- What is the difference between `on: push` and `on: pull_request`? Why do most of my other repositories' lint workflows trigger on both?
- What does `permissions: contents: read` at the top of a workflow actually restrict?
- Why should a third-party action be pinned to a commit SHA rather than a tag like `@v4`, the way my other workflows already do it?

## Why this matters to me

Every markdown-lint, gitleaks and CodeQL workflow across my other repositories started as a file exactly like this one. Understanding the shape of a workflow means I can add a genuinely new check instead of only ever copying an existing one.
