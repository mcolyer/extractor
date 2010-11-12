Extractor
========
A new package that extracts data from font binaries into objects with
the same basic API as RoboFab/defcon. Currently this only supports
OpenType/TrueType, but other formats should be relatively easy to add.

Example Use
-----------

    import os
    from robofab.world import NewFont
    from extractor import extractUFO
    
    path = "/blah/blah/blah.otf"
    destPath = os.path.splitext(path)[0] + ".ufo"
   
    dest = NewFont()
    extractUFO(path, dest)
   
    dest.save(destPath)
