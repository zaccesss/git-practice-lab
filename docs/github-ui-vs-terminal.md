# GitHub UI vs Terminal

The same task, done through the GitHub web interface and through the terminal, side by side. I default to the terminal for anything repetitive, since that is what the aliases in [practice/10-daily-workflow-and-aliases](../practice/10-daily-workflow-and-aliases) exist for. The web UI still wins for anything visual: reviewing a diff with syntax highlighting, dragging an image into a comment or a one-off setting I will not touch again for months.

| Task | GitHub web UI | Terminal |
| --- | --- | --- |
| Open an issue | Issues tab -> New issue -> pick a template | `gh issue create` or `ghissc` |
| Open a pull request | Compare & pull request button after pushing a branch | `gh pr create` or `ghprc` |
| Review a pull request | Files changed tab -> Review changes -> Comment | `gh pr review N --comment --body "..."` or `ghreview N "..."` |
| Merge a pull request | Merge pull request button, choose squash from the dropdown | `gh pr merge --squash --delete-branch` or `ghprm` |
| Delete a merged branch | Delete branch button that appears after merge | `git branch -d name` locally then `git push origin --delete name` on GitHub, `gdone` does both plus pruning in one step |
| Add a label | Labels menu in the issue or pull request sidebar | `gh issue edit N --add-label x` / `gh pr edit N --add-label x`, `ghaddlabel N x` tries both automatically |
| Create a release | Releases -> Draft a new release, pick or create a tag | `git tag -a vX.Y.Z -m "message" && git push origin vX.Y.Z`, then `gh release create` |
| Enable a branch ruleset | Settings -> Rules -> Rulesets -> New ruleset | `gh api repos/{owner}/{repo}/rulesets` for read-only inspection, rulesets themselves are UI-only to create as of writing |
| Add an image to an issue or comment | Drag and drop directly into the text box | Not possible from the terminal, `gh` has no equivalent, this is a genuinely UI-only action |
| Check a workflow run's logs | Actions tab -> the run -> the job -> the step | `gh run list` then `gh run view <id> --log` for one run, `gh run watch` for a live stream |
| Fork a repository | Fork button, top right of the repository page | `gh repo fork` or `ghfork` |
| Sync a fork with upstream | Sync fork button on the fork's own page | `git fetch upstream && git merge upstream/main` or the shorter `gh repo sync` |
| Check Community Standards | Insights tab -> Community Standards | No CLI equivalent, this checklist is UI-only |
| Set up private vulnerability reporting | Settings -> Security -> Enable private vulnerability reporting | No CLI equivalent, a one-off repository setting |

## Why I default to the terminal

Every terminal command above is scriptable, repeatable and fast once it has an alias. The web UI cannot be scripted the same way, clicking through five menus to merge a pull request does not get faster the tenth time I do it, running `ghprm` does. I reach for the UI specifically when a task genuinely needs eyes on something (a rendered diff, an image, a settings page) rather than out of habit.
