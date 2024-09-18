By arguments I mean those that begin with `--`, e.g. `--json`. 

Consider this command:

    $ fccf --enum '' . --json

It won't output json, it will output the standard format. For some time, until it's done with the current tree. And then when done with that it will try to also search in the path `--json`. And that causes a fail:

    terminate called after throwing an instance of 'std::filesystem::__cxx11::filesystem_error'
    what():  filesystem error: recursive directory iterator cannot open directory: No such file or directory []
    Aborted
