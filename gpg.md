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

## Copy GPG key to a new machine
```bash
$ gpg --export --armor KEY | ssh REMOTE_HOST 'gpg --import'
$ gpg --export-secret-key --armor KEY | ssh REMOTE_HOST 'gpg --import --allow-secret-key-import'
```
* https://blog.tomecek.net/post/import-export-private-gpg-key/

## GPG agent on remote machine
On remote machines (e.g. `mistral.dkrz.de`) it may be necessary to start the
GPG agent on the standard socket explicitly. Otherwise prompting for the
password does not work:
```bash
gpg-agent --daemon --use-standard-socket
```

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
