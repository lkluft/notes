# How to install TrueType fonts
The following approach should work on most operating systems.

1. Move TrueType fonts (TTF) to the user's font directory
   ```bash
   cp *.ttf ~/.local/share/fonts
    ```

2. Rebuild the font cache
   ```bash
   fc-cache -fv
    ```

3. (__Optional__) Remove the ``matplotlib`` font cache
   ```bash
   rm ~/.cache/matplotlib/fontList.json  # Linux
   rm ~/.matplotlib/fontlist-v300.json  # osx
   ```
