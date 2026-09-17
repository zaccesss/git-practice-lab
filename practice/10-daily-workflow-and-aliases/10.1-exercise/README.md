# 10.1: Exercise

Every command below is shown as `full command | alias`, pulled directly from [`mac/topics/04-git.zsh`](https://github.com/zaccesss/dotfiles/blob/main/mac/topics/04-git.zsh) and [`mac/topics/17-gh.zsh`](https://github.com/zaccesss/dotfiles/blob/main/mac/topics/17-gh.zsh) in my [dotfiles](https://github.com/zaccesss/dotfiles). Linux and Windows carry the same aliases in `linux/topics/` and `windows/topics/`.

## Everyday Git

| What I am doing | Full command | Alias |
| --- | --- | --- |
| Check what changed | `git status` | `gs` |
| Stage everything | `git add --all` | `gaa` |
| Commit with a message | `git commit -m "message"` | `gcmt "message"` |
| Push | `git push` | `gpsh` |
| Pull | `git pull` | `gpul` |
| Readable history | `git log --oneline --graph --decorate --all` | `glog` |
| Stage, commit and push in one step | - | `gcp "message"` |
| Start a branch fresh off an up-to-date main | `git checkout main && git pull --ff-only && git checkout -b name` | `gnb name` |
| Delete a merged local branch | `git branch -d name` | `gbd name` |
| Force-delete a local branch after a squash-merge | `git branch -D name` | `gbdf name` |
| Prune stale remote-tracking refs, locally and on origin | `git fetch --prune && git remote prune origin` | `gprune` |
| Full end-of-task reset: back on main, one branch deleted, everything pruned | - | `gdone name` |

## Everyday GitHub CLI

| What I am doing | Full command | Alias |
| --- | --- | --- |
| List open PRs | `gh pr list` | `ghprl` |
| Create a PR | `gh pr create` | `ghprc` |
| Comment on a PR | `gh pr comment` | `ghprcomment` |
| Review with a comment, my own repos only, self-approval is blocked anyway | `gh pr review N --comment --body "..."` | `ghreview N "..."` |
| Squash-merge and delete the branch | `gh pr merge --squash --delete-branch` | `ghprm` |
| Enable squash auto-merge, then let CI finish the job | `gh pr merge --squash --delete-branch --auto` | `automerge` |
| Check a PR's CI status | `gh pr checks` | `ghprchecks` |
| Create an issue | `gh issue create` | `ghissc` |
| Comment on an issue | `gh issue comment` | `ghisscomment` |
| Close an issue | `gh issue close` | `ghissclose` |
| Reopen an issue | `gh issue reopen` | `ghissreopen` |
| List a repository's real labels before applying one | `gh label list` | `ghlabels` |
| Add a label to a PR or issue, whichever it is | - | `ghaddlabel N label` |
| Full ritual: open the issue, then branch off an up-to-date main | - | `ghstart "title" label branch` |

## Steps

1. Open an issue in this repository using `ghstart` instead of the two separate GitHub-then-terminal steps I would otherwise take.
2. Make a small change, then use `gcp` to stage, commit and push it in one step.
3. Open the pull request, add the `automerge` label from the repository's real label set, then run `automerge` instead of waiting and merging by hand.
4. Once it lands, run `gdone` to land back on a clean, up-to-date `main` with the branch gone locally and on origin in one step.
5. Deliberately leave a stale local branch behind, one an IDE's Git panel created for me or one I abandoned mid-task. Confirm neither `gbd` nor `gdone` clears more than the one branch I name. See [10.2](../10.2-extra-practice) for the gap this reveals.

## Questions to answer for myself

- Why does `automerge` need both `--auto` and a passing required check to actually merge anything?
- What does `gdone` actually run underneath, in what order?
- Why is `ghreview` restricted to a comment rather than an approval on my own repositories?
