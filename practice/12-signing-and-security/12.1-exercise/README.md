# 12.1: Exercise

## SSH commit signing

Git can sign with the same kind of SSH key I already use to push, which is simpler than setting up GPG.

1. Check which key I have with `ls ~/.ssh/*.pub`. If there is none, create one with `ssh-keygen -t ed25519 -C "<my commit email>"`.
2. Tell Git to sign with it:

   ```bash
   git config --global gpg.format ssh
   git config --global user.signingkey ~/.ssh/id_ed25519.pub
   git config --global commit.gpgsign true
   git config --global tag.gpgsign true
   ```

3. On GitHub, open **Settings -> SSH and GPG keys -> New SSH key**, set **Key type** to **Signing Key** and paste the public key. The same key added once as an authentication key does not count, it has to be added again as a signing key.
4. Make a commit in this repository on a practice branch, push it and open the commit on GitHub. It should show **Verified**. If it shows **Unverified**, check the commit email matches a verified email on my account with `git log -1 --format='%ae'`.
5. Make Git able to check signatures locally by listing which keys I trust:

   ```bash
   echo "<my commit email> $(cat ~/.ssh/id_ed25519.pub)" >> ~/.ssh/allowed_signers
   git config --global gpg.ssh.allowedSignersFile ~/.ssh/allowed_signers
   ```

6. Run `git log --show-signature -1` and `git verify-commit HEAD` and read what each one reports.

## Questions to answer for myself

- What exactly does a signature prove? What does it not prove about the code inside the commit?
- Why does GitHub need the key added as a signing key when it already knows it as an authentication key?
- What would `git verify-commit` say about a commit signed by a key missing from `allowed_signers`?
