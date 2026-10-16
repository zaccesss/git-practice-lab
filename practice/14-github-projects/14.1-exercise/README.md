# 14.1: Exercise

## Steps

1. Give the GitHub CLI access to projects, which it does not have by default: `gh auth refresh -s project`.
2. Create a project owned by my account: `gh project create --owner "@me" --title "Git Practice Lab"`. Note the number it prints.
3. Open three issues in this repository, one for each module I still have to work through, then add each to the project:

   ```bash
   gh project item-add <number> --owner "@me" --url https://github.com/zaccesss/git-practice-lab/issues/<issue>
   ```

4. In the browser, add a **Board** view grouped by **Status** and move one item to **In Progress**.
5. Add two custom fields: **Priority** as a single select (High, Medium, Low) and **Size** as a number. Fill both in for each item.
6. Open the project's **Workflows** page and check the built-in workflows that set **Status** to **Done** when an item is closed or its pull request is merged.
7. Close one of the issues through a merged pull request and watch its card move to **Done** on its own.
8. Link the project to this repository from the repository's **Projects** tab so it shows up there.

## Questions to answer for myself

- Why does a project live on my account or an organisation instead of inside one repository?
- What is the difference between a label on an issue and a field on a project item?
- Which of the built-in workflows saves me the most manual work? Which would I turn off?
