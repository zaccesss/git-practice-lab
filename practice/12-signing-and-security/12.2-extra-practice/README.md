# 12.2: Extra Practice

1. **Signed tags:** create an annotated tag with `git tag -s v0.0.1-practice -m "practice tag"`, check it with `git tag -v v0.0.1-practice`, then delete it locally with `git tag -d v0.0.1-practice`.
2. **Vigilant mode:** read what **Flag unsigned commits as unverified** in **Settings -> SSH and GPG keys** changes. Note why it marks every unsigned commit of mine as **Unverified** once it is on.
3. **Signing on GitLab:** add the same public key on GitLab under **Edit profile -> SSH Keys** with **Usage type** set to signing, push a signed commit to the project from [module 11](../../11-gitlab) and find its badge there.
4. **Ignoring secrets:** in a throwaway repository, add `.env` to `.gitignore`, create a `.env` file with a made-up value and confirm `git status` no longer lists it. Then run `git check-ignore -v .env` to see which rule matched.
5. **Push protection:** read how GitHub's secret scanning push protection blocks a push that contains a recognised token, what the bypass options are and why a bypass still raises an alert. Never test it with a real token.
6. **A leaked secret drill:** write down, in order, what I would do if a real token reached a public repository: revoke it at the provider first, replace it, then decide whether rewriting history is still worth it.

## Questions to answer for myself

- Why does `.gitignore` do nothing for a file Git is already tracking? How do I stop tracking it without deleting it?
- Why is revoking a leaked token more urgent than removing it from the history?
- What does a signed tag add to a release that a signed commit alone does not?
