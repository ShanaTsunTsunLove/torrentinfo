Welcome to torrentinfo's documentation!
***************************************

This documentation aims to provide at least an overview of what to expect when using or scripting against torrentinfo.

About
=====

`torrentinfo` parses .torrent files and displays information about the torrent
and the files that it references. On the default basic setting it shows:

 - Torrent name
 - Tracker URL
 - The creator of the torrent
 - The torrent's creation date
 - The number of files (if a multi-file torrent)
 - The name of the file (if a single-file torrent)
 - The total size of the file/files

If asked to display file information the path and size of each file is
listed.

Additionally the entire torrent can be shown in hierachical form.

Why fork?
=========

I forked the original project simply because it was missing functionality I
desired, namely what the `-t` flag does now. It turned out that the code
was an undocummented mess but it worked so no one bothered. It was no longer
listed on the creators website and the original creator was surprised that
anyone even found it useful. For this reason I decided to the dust off the
project, clean it up, document it and provide a few tests along the way.

I'm keeping the original name of the project in case someone (like me) finds
themself in a similar position and does a Google search for "torrentinfo".

Usage
=====

``usage: torrentinfo [-h] [-v] [-t | -f | -d] [-a] [-n] filename [filename ...]``::

  Print information about torrent files

  positional arguments:
    filename        Torrent files to process

  optional arguments:
    -h, --help        show this help message and exit
    -v, --version     Print version and quit
    -t, --top         Only show top level file/directory
    -f, --files       Show files within the torrent
    -d, --detailed    Print more information about the files
    -e, --everything  Print everything we can about the torrent
    -a, --ascii       Only print out ascii
    -n, --nocolour    No ANSI colour


If no settings are specified the script will default to showing the basic
information on each file.

Install
=======

TorrentInfo uses the standard Python distribution utilities. So it should just
be a case of uncompressing the archive and running::

    ./setup.py install

The user running this must have sufficient permissions to create a
file in the install directory.

Bugs
====

Any bugs or fixes should be submitted to `my GitHub <https://github.com/Fuuzetsu/torrentinfo>`_.

Credits
=======

I like to give credit where it's due. `Vrai Stacey <http://vrai.net>`_ is the original creator but no longer maintains the project .

torrentinfo
===========

.. toctree::
   :maxdepth: 2

.. automodule:: torrentinfo
   :members:
