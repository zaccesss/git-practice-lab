# Command Reference

Every command that shows up across the practice modules, explained properly. The root [README](../README.md) stays short on purpose, this is where the actual detail lives. See [glossary.md](glossary.md) if a term itself, rather than a command, is unclear.

## The everyday loop

| Command | What it actually does |
| --- | --- |
| `git status` | Compares the working directory, the staging area and the last commit, reporting what is untracked, modified or staged |
| `git add <file>` | Copies a file's current content into the staging area, ready for the next commit |
| `git add --all` | Stages every change in the repository, new, modified and deleted files alike |
| `git diff` | Shows the difference between the working directory and the staging area, what would be added if I staged everything right now |
| `git diff --staged` | Shows the difference between the staging area and the last commit, what the next commit will actually contain |
| `git commit -m "message"` | Creates a new commit from whatever is currently staged, with the given message |
| `git commit --amend` | Replaces the last commit entirely, either its message, its content or both, rather than creating a new one |
| `git log --oneline` | Shows commit history as one line per commit, hash and message only |
| `git log --oneline --graph --decorate --all` | The same, but drawn as a branch graph with every branch and tag labelled |
| `git push` | Uploads local commits on the current branch to its configured remote |
| `git pull` | Downloads remote commits and merges them into the current branch in one step |

## Branching

| Command | What it actually does |
| --- | --- |
| `git branch` | Lists local branches, the current one marked with `*` |
| `git branch <name>` | Creates a new branch pointing at the current commit, without switching to it |
| `git checkout -b <name>` | Creates a new branch and switches to it in one step, the older syntax |
| `git switch -c <name>` | The same as above, using the newer, more explicit `switch` command |
| `git branch -d <name>` | Deletes a local branch, refusing if it has commits not yet merged anywhere |
| `git branch -D <name>` | Force-deletes a local branch regardless of merge status, needed after a squash-merge since Git cannot tell it was merged |
| `git branch -m <new-name>` | Renames the current branch |
| `git branch --merged` | Lists branches already fully merged into the current one, safe to delete |
| `git branch --no-merged` | Lists branches with commits not yet merged in, a warning before deleting |

## Undoing things

| Command | What it actually does |
| --- | --- |
| `git restore <file>` | Discards uncommitted changes to a file, reverting it to the last commit |
| `git restore --staged <file>` | Unstages a file without touching its content, the opposite of `git add` |
| `git reset HEAD~1` | Moves the current branch back one commit, keeping the changes staged |
| `git reset --hard HEAD~1` | Moves the current branch back one commit and discards the changes entirely |
| `git revert <hash>` | Creates a new commit that undoes a previous one, safe on shared history since nothing already pushed is rewritten |

## Merging and rebasing

| Command | What it actually does |
| --- | --- |
| `git merge <branch>` | Combines another branch into the current one, creating a merge commit if the histories diverged |
| `git merge --abort` | Cancels an in-progress merge, restoring the state from before it started |
| `git rebase <branch>` | Replays the current branch's commits on top of another branch, producing new commit hashes |
| `git rebase -i HEAD~<n>` | Opens an interactive rebase covering the last `n` commits, for squashing, reordering or editing |
| `git rebase --continue` | Resumes a rebase after resolving a conflict or finishing an `edit` stop |
| `git rebase --abort` | Cancels an in-progress rebase entirely, restoring the branch to where it started |

## Stash and cherry-pick

| Command | What it actually does |
| --- | --- |
| `git stash` | Shelves uncommitted changes and restores a clean working directory |
| `git stash push -m "message"` | The same, with a description so `git stash list` stays readable |
| `git stash list` | Lists everything currently shelved |
| `git stash pop` | Reapplies the most recent stash and removes it from the list |
| `git stash apply` | Reapplies the most recent stash without removing it from the list |
| `git cherry-pick <hash>` | Copies a single commit from elsewhere onto the current branch, as a new commit |

## Remotes

| Command | What it actually does |
| --- | --- |
| `git remote -v` | Lists configured remotes and their URLs |
| `git remote add <name> <url>` | Adds a new named remote |
| `git fetch <remote>` | Downloads a remote's commits without merging them into anything |
| `git fetch --prune` | Fetches and also removes local references to branches deleted on the remote |
| `git push origin --delete <branch>` | Deletes a branch on the remote, not just locally |

## Diagnosing history

| Command | What it actually does |
| --- | --- |
| `git reflog` | Shows every commit `HEAD` has pointed at locally, the recovery tool for a bad rebase or reset |
| `git bisect start` | Begins a binary search through history to find which commit introduced a bug |
| `git show <hash>` | Shows exactly what one commit changed |

## GitHub CLI (`gh`)

| Command | What it actually does |
| --- | --- |
| `gh pr create` | Opens a pull request from the current branch, interactively or with flags |
| `gh pr list` | Lists open pull requests in the current repository |
| `gh pr checkout <number>` | Checks out someone else's pull request locally by number |
| `gh pr review <number> --comment --body "..."` | Leaves a review comment on a pull request without approving or requesting changes |
| `gh pr merge --squash --delete-branch` | Squash-merges the current branch's pull request and deletes the branch, locally and on GitHub |
| `gh pr merge --squash --delete-branch --auto` | The same, but enabled ahead of time, so it fires automatically once required checks pass |
| `gh pr checks` | Shows the status of every check on a pull request |
| `gh issue create` | Opens a new issue |
| `gh issue close` | Closes an issue directly, without needing a linked pull request |
| `gh label list` | Lists every label that actually exists on the current repository |
| `gh run watch` | Streams a running workflow's logs live in the terminal |

See [practice/10-daily-workflow-and-aliases](../practice/10-daily-workflow-and-aliases) for the shorter alias I actually type for most of the commands above.
