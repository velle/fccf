
If foobar is not a directory or cpp/h file. 





But!!! In all other cases, it gives the following error:

    $ fccf --enum '' foobar
    terminate called after throwing an instance of 'std::filesystem::__cxx11::filesystem_error'
    what():  filesystem error: recursive directory iterator cannot open directory: No such file or directory []
    Aborted

When foo.txt is a file with random text:

    $ fccf --enum '' foobar
    terminate called after throwing an instance of 'std::filesystem::__cxx11::filesystem_error'
    what():  filesystem error: recursive directory iterator cannot open directory: No such file or directory []
    Aborted

When foo.txt is a valid cpp file renamed to 



terminate called after throwing an instance of 'std::filesystem::__cxx11::filesystem_error'
  what():  filesystem error: recursive directory iterator cannot open directory: No such file or directory []
Aborted