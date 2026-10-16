# 11.1: Exercise

## The GitHub words and their GitLab equivalents

| GitHub | GitLab |
| --- | --- |
| Repository | Project |
| Organisation | Group |
| Pull request | Merge request (MR) |
| Actions workflow in `.github/workflows/` | Pipeline in `.gitlab-ci.yml` at the project root |
| Check | Pipeline job |
| Branch protection or a ruleset | Protected branch |
| `gh` | `glab` |

## Steps

1. Install the GitLab CLI with `brew install glab`, then sign in with `glab auth login` and confirm it with `glab auth status`.
2. Create a throwaway project from the terminal: `glab repo create gitlab-practice --private`, then clone it.
3. In the project, open **Settings -> Repository -> Protected branches** and check `main` is protected with **Allowed to push and merge** set to Maintainers. Try `git push origin main` from a commit on `main` to see what the protection does and does not stop for my own role.
4. Copy [example-gitlab-ci.yml](example-gitlab-ci.yml) into the project root as `.gitlab-ci.yml`, plus a `practice` folder with a file or two in it so the count job has something to count.
5. Open an issue with `glab issue create`, note its number, then start a branch for it: `git switch -c feature/first-pipeline`.
6. Commit the pipeline file, push the branch, then open the merge request from the terminal with `glab mr create --fill --target-branch main`. Put `Closes #1` (with the real issue number) in the description.
7. Watch the pipeline with `glab ci status`, then open the full view with `glab ci view` and read each job's log.
8. Merge it from the terminal with `glab mr merge --squash --remove-source-branch`, then check the issue closed itself.
9. Clean up locally the same way as on GitHub: `git switch main`, `git pull --ff-only`, `git branch -D feature/first-pipeline` and `git fetch --prune`.

## Questions to answer for myself

- Why does a GitLab job start in a fresh container with none of the previous stage's files unless they are passed on as artifacts?
- What exactly did the protected branch stop? Would it stop a Developer where it did not stop me?
- What does the `workflow: rules:` block in the example file prevent? What would happen on an open merge request without it?
