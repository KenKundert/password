Password Generator
==================

This repository has moved! The password generator project now has a name: 
Abraxas. As such, the repository itself has been renamed.

If you would like to clone the new Abraxas repository, use::

    git clone git@github.com:KenKundert/abraxas.git

If you currently have a repository and would like to retarget it to the new 
Abraxas repository, change your working directory to one that is inside your 
existing repository and run::

    git remote set-url origin git@github.com:KenKundert/abraxas.git

If you currently use pw, take these steps to convert to Abraxas:

#. As you (not root) run the following commands to uninstall the existing 
   version of pw::

      rm -f ~/.local/bin/pw ~/.local/man/man?/pw.?
      rm -rf ~/.local/lib/python[23]*/site-packages/pw-*.egg

#. Move to the directory that contains pw and change its name to abraxas::

      mv pw abraxas

#. Move into the abraxas directory and update and install the program::

      cd abraxas
      git pull

#. Rename the config directory::

      mv ~/.config/pw ~/.config/abraxas

#. Edit your accounts files and change the charsets import from::

      from pw.charstets import (

   to::

      from abraxas.charstets import (

   Then edit the log_file and archive_file settings in the accounts file and 
   change pw to abraxas.

#. Finally, edit the hot key setting for your window manager so that it runs::

      ~/.local/bin/abraxas --autotype

   rather than::

      ~/.local/bin/pw --autotype

-Ken
