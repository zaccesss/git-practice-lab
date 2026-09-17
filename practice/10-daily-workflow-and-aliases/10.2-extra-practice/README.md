# 10.2: Extra Practice - Finding My Own Gaps

The point of this module is not just using my existing aliases, it is noticing where one is missing. I found two while writing [10.1](../10.1-exercise), not before:

- **No bulk cleanup for merged local branches.** `gdone` deletes exactly one named branch. A stale branch an IDE created for me (VS Code's Git Graph panel, for example) sits locally forever unless I name it directly.
- **No terminal-to-browser quick search.** A `google "query"` style alias that opens Chrome straight to a search results page does not exist yet, an idea from an earlier session that never made it into `dotfiles`.

Neither belongs in this repository, they belong in `dotfiles` itself. This module is where I practise the process of closing a gap like that, using the first one as a worked example.

## Steps

1. Write the raw command that lists every local branch already merged into `main`, excluding `main` itself: `git branch --merged main | grep -v '\* \|main'`.
2. Confirm it actually lists a real stale branch by creating one, merging it and leaving it undeleted.
3. Pipe that list into `xargs -r git branch -d` and confirm it deletes every merged branch in one step.
4. Turn that into a shell function called `gclean-branches` in a scratch file, following the same style as the existing functions in `mac/topics/04-git.zsh` (a short comment above it explaining why it exists).
5. If this genuinely belongs in `dotfiles`, follow the same issue-to-PR workflow I use everywhere else to add it there, not here.

## Questions to answer for myself

- Why does `gbd` deliberately refuse to delete more than one branch at a time, is that a limitation or a safety feature?
- What would `gclean-branches` do to a branch that is merged into `main` but that I actually still wanted to keep around for reference?
- What other daily command do I reach for often enough that it deserves its own alias, that is not on this list?
