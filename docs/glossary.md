# Glossary

Plain definitions for every term used across the practice modules, Git and GitHub side by side. My [git-unlocked](https://github.com/zaccesss/git-unlocked) repository has a much larger [full glossary](https://github.com/zaccesss/git-unlocked/blob/main/09-reference/glossary.md) covering other platforms too, this one stays scoped to what actually appears in this repository.

## Git terms

**Working directory**
The actual files on disk as I am editing them, before anything is staged.

**Staging area (the index)**
Where a change sits after `git add` and before `git commit`, a holding area for exactly what the next commit will contain.

**Commit**
A saved snapshot of the staged changes, with a message, an author and a parent commit, forming the chain that is the project's history.

**Branch**
A movable pointer to a commit. Creating a branch does not copy anything, it just gives a new name to build on from the current commit.

**HEAD**
Whatever commit I currently have checked out. Usually `HEAD` points at a branch, which in turn points at a commit, moving the branch pointer forward with every new commit.

**Merge**
Combining two branches' histories into one, creating a new commit with two parents where they meet.

**Rebase**
Replaying one branch's commits on top of another, producing new commit hashes and a straight-line history instead of a merge commit.

**Merge conflict**
What happens when Git cannot automatically decide how to combine two changes to the same lines, requiring a human to choose.

**Stash**
A temporary shelf for uncommitted changes, letting me switch context without committing half-finished work.

**Cherry-pick**
Copying a single commit from one branch onto another, without merging or rebasing the whole branch.

**Reflog**
A local, personal log of everywhere `HEAD` has pointed, even commits no branch references any more. My safety net for recovering from a bad rebase or an accidental branch deletion.

**Bisect**
A binary search through commit history to find the exact commit that introduced a bug, using `good` and `bad` markers.

**Worktree**
A second working directory checked out from the same repository, letting me have two branches open side by side without cloning twice.

**Restore**
Putting a file back to how it was in the staging area or a commit, without moving any branch. `git restore` replaced the file-level uses of `git checkout`.

**Reset**
Moving the current branch to another commit. `--soft` keeps the changes staged, `--mixed` (the default) keeps them unstaged and `--hard` throws them away.

**Revert**
A new commit that undoes an earlier one, the safe undo for anything already pushed because no existing history is rewritten.

**Detached HEAD**
Checking out a commit directly rather than a branch. New commits made there belong to no branch until one is created for them.

**Signed commit**
A commit carrying a cryptographic signature from a GPG or SSH key, which GitHub and GitLab show as Verified when the key is on the author's account.

**Partial clone**
A clone that skips some objects, such as file contents with `--filter=blob:none`. It fetches them later when needed or with `git backfill`.

**Remote**
A named reference to another copy of the repository, usually on GitHub. `origin` and `upstream` are conventional names, not special keywords.

**Fork**
A personal copy of someone else's repository on GitHub, used to contribute without write access to the original.

## GitHub terms

**Issue**
A tracked unit of work or discussion, not tied to a specific branch or commit until one references it.

**Pull request**
A request to merge one branch into another, with a diff, a discussion thread and checks attached, GitHub's name for what other platforms call a merge request.

**Draft pull request**
A pull request marked not ready for review yet, visible and testable but excluded from review queues until marked ready.

**Label**
A tag applied to an issue or pull request for filtering and triage, defined per repository, never guessed.

**CODEOWNERS**
A file that automatically requests a review from the named people or teams whenever a matching path changes in a pull request.

**Issue template (YAML form)**
A structured form, defined in `.github/ISSUE_TEMPLATE/*.yml`, that replaces a free-text issue body with defined fields.

**config.yml (issue template config)**
The file in `.github/ISSUE_TEMPLATE/` that controls the template chooser itself, for example disabling the blank-issue option or adding external contact links.

**GitHub Actions workflow**
A YAML file in `.github/workflows/` describing jobs that run automatically on events like a push or a pull request.

**Required check**
A status check a repository's rules require to pass before a pull request can merge, distinct from a check that merely reports its result.

**Auto-merge**
A pull request setting that merges it automatically the moment its required checks pass, without anyone needing to click merge by hand.

**Automerge label**
Not a GitHub built-in, a convention used across my own repositories: applying an `automerge` label tells my `repo-ops` automation to enable auto-merge on that pull request.

**Merge queue**
A GitHub feature that serialises several pull requests landing on a busy branch, re-testing each one against the latest state before it merges rather than trusting a check result from before the branch moved.

**Stacked pull request**
A pull request that targets another still-open pull request's branch instead of `main`, used to break one large change into reviewable, dependent pieces.

**Ruleset**
GitHub's newer, more flexible replacement for classic branch protection, expressed as named rules that can target multiple branches or tags at once.

**GitHub release**
A published, citable snapshot built on top of a Git tag, with release notes and optional binary assets attached.

**GitHub Discussions**
A forum-style space for open-ended conversation, separate from issues, meant for questions and ideas rather than tracked work.

**Codespaces**
A full cloud development environment tied to a repository, configurable so it opens with the right tools already installed.

**Private vulnerability reporting**
GitHub's built-in flow letting someone report a security issue privately through the Security tab, without needing a separate email address.

**Sub-issue**
An issue attached to a parent issue, so the parent shows progress as its children close.

**GitHub Project**
A planning board or table that lives on an account or organisation and pulls in issues and pull requests from any of its repositories.

**Push protection**
Secret scanning that blocks a push containing a recognised token before it reaches GitHub.

**Vigilant mode**
An account setting that marks every unsigned commit of mine as Unverified, so a commit made in my name without my key stands out.

**Release attestation**
A signed statement from GitHub about a release and its assets, checked with `gh release verify`.

## GitLab terms

**Project**
GitLab's name for a repository plus everything around it: issues, merge requests, pipelines and settings.

**Group**
GitLab's equivalent of an organisation, holding projects and subgroups with shared members and permissions.

**Merge request (MR)**
GitLab's name for a pull request.

**Pipeline**
A run of the jobs defined in `.gitlab-ci.yml`, grouped into stages that run in order.

**Job**
One task in a pipeline, run by a runner, usually in a fresh container.

**Runner**
The machine or container that picks up pipeline jobs and runs them.

**Artifact**
Files a job saves so a later stage or a person can use them.

**Protected branch**
A branch only chosen roles can push or merge to, GitLab's equivalent of branch protection.

**glab**
The official GitLab CLI, GitLab's equivalent of `gh`.

## See also

- [docs/command-reference.md](command-reference.md) - every command in this repository, explained in full
- [docs/github-ui-vs-terminal.md](github-ui-vs-terminal.md) - the same task, shown both ways
