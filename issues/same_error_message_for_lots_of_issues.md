There are lots of ways in which one can give invalid parameters / paths on command line. And lots of them result in this error, which does not help af whole lot:

    $ fccf --enum '' foobar
    terminate called after throwing an instance of 'std::filesystem::__cxx11::filesystem_error'
    what():  filesystem error: recursive directory iterator cannot open directory: No such file or directory []
    Aborted
