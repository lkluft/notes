# Using customg colormaps in ``ncview``

1. Export a Python colormap (here ``viridis``) using typhon:

   ```python
   from numpy import savetxt
   from typhon.plots import cmap2rgba


   colors = cmap2rgba('viridis')
   savetxt('viridis.ncmap', 255 * colors[:, :3], fmt='%d')
   ```

2. Store the file ``viridis.ncmap`` in any directory (here ``MY_DIR``).

3. ``ncview`` examines the user's environmental variable ``NCVIEWBASE``
   for the name of a directory which contains additional colormap files

   ```bash
   export NCVIEWBASE=MY_DIR
   ncview
   ```
