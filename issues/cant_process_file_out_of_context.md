It is possible to pass a path for a specific file (cpp or h):

    $ fccf --enum ''  core/qgsapplication.cpp

One can even rename it and give it a different extension, and there are no problems:

    $ cp  core/qgsapplication.cpp core/funky.txt
    velle@velle-ThinkPad-W530:~/a/QGIS/src$

But if we move it to a different location, together with header, it will fail. 

    cp core/qgsapplication.* .
    fccf --enum ''  baz.cpp

So I guess the code has to be kind of valid. It is likely not able to search a random cpp file that comes out of context. Maybe that's because of precompilation of macros ...?
