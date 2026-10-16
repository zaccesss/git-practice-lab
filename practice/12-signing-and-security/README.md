# 12: Signing and Security

I use this module to practise proving my commits are mine and keeping secrets out of a repository in the first place.

| Part | What it covers |
| --- | --- |
| [12.1: Exercise](12.1-exercise) | SSH commit signing, the Verified badge and checking signatures locally |
| [12.2: Extra Practice](12.2-extra-practice) | Signed tags, vigilant mode, signing on GitLab, ignoring secrets and push protection |
| [12.3: Self-Test](12.3-self-test) | Questions with no answers shown, to check what actually stuck |

## Why this matters to me

Git trusts whatever name and email I put in my config, so anyone can write a commit that claims to be from me. A signature is the proof. Secrets are the other half: once a token is pushed it has to be treated as leaked, however quickly the commit is removed. Both habits cost a few minutes to set up and save a much worse afternoon later.
