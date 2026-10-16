# 11.2: Extra Practice

1. **Merge methods:** in **Settings -> Merge requests**, switch the project between a merge commit, a merge commit with semi-linear history and a fast-forward merge. Merge one small merge request under each and compare the history with `git log --oneline --graph`.
2. **Draft merge requests:** open a merge request with `Draft:` at the start of its title and confirm it cannot be merged until I mark it ready.
3. **Suggested changes:** review my own merge request in the **Changes** tab, leave a suggestion on one line, then apply it from the browser and pull the commit it creates.
4. **Pipeline rules:** add a job with `rules:` so it only runs on `main`, then confirm from a merge request pipeline that it was skipped.
5. **CI variables:** add a masked variable under **Settings -> CI/CD -> Variables** (a made-up value, never a real secret), print it from a job and confirm the log shows it masked.
6. **Validate before pushing:** break the pipeline file on purpose, then run `glab ci lint` to catch the mistake locally before GitLab does.
7. **Push mirroring:** read how a GitLab project can push-mirror to another remote or pull from one, the same idea that keeps copies of my GitHub repositories on other platforms.

## Questions to answer for myself

- Which merge method keeps the history straightest? What does it make me do before every merge?
- Why does GitLab mask a variable in the log instead of refusing to print it at all?
- When would I pick a merge request pipeline over a branch pipeline?
