Extractor
=====================================

A new package that extracts data from font binaries into objects with
the same basic API as RoboFab/defcon. Currently this only supports
OpenType/TrueType, but other formats should be relatively easy to add.

It requires `robofab <http://www.robofab.org>`_ to run.

The latest development snapshot can be found in the `subversion repository <http://svn.typesupply.com/packages/extractor/trunk/>`_.

Example
---------------

::

    import os
    from robofab.world import NewFont
    from extractor import extractUFO

    path = "/blah/blah/blah.otf"
    destPath = os.path.splitext(path)[0] + ".ufo"

    dest = NewFont()
    extractUFO(path, dest)

    dest.save(destPath)

API Reference
==================

.. toctree::
   :maxdepth: 1

   objects/base


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

