# Set up OSX - Notes

## General configuration

1. Install MacPorts ports using:
   ```bash
   $ sudo port install $(cat ports.txt)
   ```

2. Add `/opt/local/bin/bash` to list of standard shells in `/etc/shells`.
   Change default shell using `chsh`.

3. Create symbolic links `~/bin/vim` and `~/bin/gvim` for MacVim.

4. Initialiaze submodules after cloning `vim.git` from GitHub.
   ```bash
   $ git submodule update --init --recursive --remote
   ```

5. Turn off system sounds
   ```
   System Preferences -> Sound -> Play user interface sound effects
   ```

6. Prevent hard disks from sleep when charging. This keeps network connections
   going when unsed in "docking" mode.
   ```
   System Preferences -> Energy Saver -> Battery
   -> Put hard disks to sleep when possible
   ```

## List of installed MacPorts

bash
bash-completion
cmake
coreutils
gcc8
git +svn
gnupg2
gsed
gtime
tmux
tree
wget
watch
p5-file-rename
xpdf-tools

## Applications

* Chrome
* Dropbox
* KeePassXC
* MacPorts
* MacTex
* Spotify
* XCode
* XQuartz
* osxfuse
* sshfs
* Texmaker
* Panoply
* Acrobat Reader
