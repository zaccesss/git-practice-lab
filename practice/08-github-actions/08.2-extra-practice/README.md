# 08.2: Extra Practice

1. Add a matrix to the practice workflow so `count-files` runs on `ubuntu-latest`, `macos-latest` and `windows-latest` at once: `strategy: matrix: os: [ubuntu-latest, macos-latest, windows-latest]` then `runs-on: ${{ matrix.os }}`.
2. Add a `concurrency` group so pushing twice in quick succession cancels the first run, the same pattern `competitive-programming`'s `sync.yml` uses for a burst of pushes.
3. Upload a file as a build artifact with `actions/upload-artifact`, download it in a later job with `actions/download-artifact`. Confirm the second job can actually read what the first one produced.
4. Store a fake secret in the repository's Actions secrets settings, reference it as `${{ secrets.MY_SECRET }}` in a step. Confirm the logs mask it automatically even if I try to print it.
5. Add a manual approval gate using a GitHub Environment with required reviewers, then trigger a workflow that targets it and watch it pause for approval.
6. Write a second, reusable workflow file (`workflow_call` as the trigger) and call it from the practice workflow with `uses: ./.github/workflows/reusable.yml`.

## Questions to answer for myself

- Why does a matrix multiply job runs rather than running once with a variable, what is actually happening underneath?
- What is the actual security benefit of GitHub automatically masking a secret in logs, what does it not protect me from?
- When would a reusable workflow be worth the extra indirection over just duplicating the steps in two files?
