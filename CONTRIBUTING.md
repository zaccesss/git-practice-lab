# Professional GitHub Workflow

Use this workflow for every meaningful coding session. The goal is to build professional habits: plan the work, isolate changes on a branch, review the diff, merge through a pull request, and keep `main` clean.

## Standard Session Workflow

### 1. Create an Issue

Before coding, create a GitHub issue that describes the work.

- Go to the repository on GitHub.
- Open the **Issues** tab.
- Click **New issue**.
- Use a clear title, such as `Add telemetry dashboard` or `Fix auth validation`.
- Add a short description explaining what needs to change.
- Add a relevant label: `enhancement`, `bug`, `docs`, or `refactor`.
- Note the issue number, such as `#5`.

### 2. Create a Branch

Create a branch from `main` for the issue.

```powershell
git checkout main
git pull
git checkout -b feature/description-of-work
```

Common branch prefixes:

| Prefix | Use for |
| --- | --- |
| `feature/` | New functionality |
| `fix/` | Bug fixes |
| `docs/` | Documentation updates |
| `refactor/` | Code improvements without feature changes |
| `solve/` | Competitive programming solutions |

Examples:

```powershell
git checkout -b feature/telemetry-dashboard
git checkout -b fix/auth-validation
git checkout -b docs/readme-update
git checkout -b solve/347-top-k-frequent-elements
```

### 3. Do the Work

Make the code or documentation changes, then test them locally.

```powershell
git status
git add .
git commit -m "Describe what changed"
```

Prefer clear commit messages that explain the result of the change, not just the file that changed.

### 4. Push the Branch

```powershell
git push origin feature/your-branch-name
```

Replace `feature/your-branch-name` with the actual branch name.

### 5. Open a Pull Request

On GitHub:

- Open the **Pull requests** tab.
- Click **New pull request**.
- Set `base` to `main`.
- Set `compare` to your feature branch.
- Use the issue title as the PR title.
- In the description, link the issue with `closes #NUMBER`.

Example PR description:

```text
closes #5

Adds the telemetry dashboard and updates the README with usage notes.
```

Using `closes #NUMBER` automatically closes the linked issue when the PR is merged.

### 6. Review the Diff

Before merging, read through the PR diff.

Check for:

- Accidental files.
- Unclear code.
- Missing tests or manual checks.
- README or documentation updates.
- Sensitive information such as tokens, emails, or local paths.

If useful, leave a short comment explaining a decision. This builds the habit of thinking like a reviewer.

### 7. Merge the Pull Request

When the PR is ready:

- Click **Merge pull request**.
- Click **Confirm merge**.
- Delete the remote branch when GitHub offers the option.

### 8. Clean Up Locally

```powershell
git checkout main
git pull
git branch -d feature/your-branch-name
```

This keeps the local repository in sync with GitHub.

## What This Creates

Instead of only creating commits, each work session creates a linked record:

- One issue showing the planned work.
- One branch showing isolated development.
- One or more commits showing the actual changes.
- One pull request showing review and merge history.

This makes the project history easier to follow and demonstrates a professional development workflow.

## Project Examples

### Competitive Programming Repositories

Use this for LeetCode, NeetCode, Codeforces, and similar repos.

- Issue title: `Solve [ProblemName] - [Difficulty]`
- Label: `enhancement`
- Branch: `solve/[problem-code-or-name]`
- Example issue: `Solve Contains Duplicate - Easy`
- Example branch: `solve/contains-duplicate`
- Example PR description: `closes #7 - Adds Python, C++, and Java solutions with complexity notes.`

### Feature Projects

Use this for larger projects such as dashboards, platforms, APIs, and apps.

- Issue title: `Add [feature name]`
- Labels: `enhancement`, `feature`
- Branch: `feature/[feature-name]`
- Example issue: `Add real-time alerts system`
- Example branch: `feature/real-time-alerts`

### Documentation Updates

- Issue title: `Update [section] documentation`
- Label: `docs`
- Branch: `docs/[what-was-updated]`
- Example issue: `Update installation instructions`
- Example branch: `docs/installation-guide`

### Bug Fixes

- Issue title: `Fix [bug description]`
- Label: `bug`
- Branch: `fix/[bug-name]`
- Example issue: `Fix authentication token expiry`
- Example branch: `fix/token-expiry`

## Code Review Habits

For solo projects, review your own PR before merging. For stronger practice, review other people's code too.

Good review comments are specific and useful. Examples:

- `Could this use a dictionary instead of a list to reduce lookup time?`
- `This function is doing validation and formatting. Should those be split?`
- `What happens here if the API response is empty?`
- `Can we add a short test for this edge case?`

Avoid empty comments such as `looks good` unless you have already checked the code carefully.

## Open Source Practice

To practise real external review:

- Find a repository you use or understand.
- Look for issues labelled `good first issue` or `help wanted`.
- Make a small focused change.
- Open a PR with a clear description.
- Respond professionally to review comments.

## Full Example Session

Issue already created:

```text
#42 Solve Top K Frequent Elements - Medium
```

Terminal:

```powershell
git checkout main
git pull
git checkout -b solve/347-top-k-frequent-elements

# Write the solution files.

git add .
git commit -m "Solve LeetCode 347 with hash map approach"
git push origin solve/347-top-k-frequent-elements
```

GitHub PR:

```text
Title: Solve Top K Frequent Elements - Medium

closes #42

Adds Python, C++, and Java solutions with time and space complexity notes.
```

After merge:

```powershell
git checkout main
git pull
git branch -d solve/347-top-k-frequent-elements
```

## Rule Going Forward

For meaningful changes, use:

```text
issue -> branch -> commit -> push -> pull request -> review -> merge -> cleanup
```

Small typo fixes can be committed directly when appropriate, but features, fixes, documentation updates, and learning exercises should use the full workflow.
