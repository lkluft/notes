# Generating a GPG Key
1. Download and install the latest GPG command line tools (macports: `gnupg2`).
2. Generate a GPG key pair:
   ```bash
   $ gpg --full-generate-key
   ```

   Use the default `RSA and RSA` key and a length of `4096`.
   
   **Note: The email used for the GPG key has to match your GitHub email.**
3. Export the public key:
   ```bash
   gpg --armor --export
   ```

   _You may have to specify a real name, key id or email._
* https://help.github.com/articles/generating-a-new-gpg-key/

# Signing git commits using GPG
1. Add the GPG key to your GitHub account.
2. To sign all commits by default in any repository on your computer, run:
    ```bash
    $ git config --global commit.gpgsign true
    ```
    Make sure that `git` associates your commits with the proper email
    (`git config --global user.email`). The email is used to determine
    which GPG key to use.
* https://help.github.com/articles/signing-commits-using-gpg/
