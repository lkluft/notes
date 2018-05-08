# Generating a GPG Key

1. Download and install the latest GPG command line tools (macports: `gnupg2).
2. Generate a GPG key pair:

   ```bash
   $ gpg --full-generate-key
   ```

   Use the default `RSA and RSA` key and a length of `4096`.

3. Export the public key:

   ```bash
   gpg --armor --export 
   ```

   You may have to specify a real name, key id or email.
