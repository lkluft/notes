# Where to find fonts?
You can use [Google Fonts](https://github.com/google/fonts) to find and
download various open source fonts. It is even possible to download their whole
archive (https://github.com/google/fonts/tarball/master).

# How to install TrueType fonts
The following approach should work on most operating systems.

1. Move TrueType fonts (TTF) to the user's font directory.
   (It is possible to keep them in subdirectories for tidiness.)
   ```bash
   cp *.ttf ~/.local/share/fonts
    ```

2. Rebuild the font cache
   ```bash
   fc-cache -fv
    ```

3. (_Optional_) Remove the ``matplotlib`` font cache
   ```bash
   rm ~/.cache/matplotlib/fontList.json  # Linux
   rm ~/.matplotlib/fontlist-v300.json  # osx
   ```
