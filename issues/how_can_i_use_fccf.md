I could dump everything to json, absolutely everything. 

    $ time fccf --json . > everything.json
    fccf: /home/velle/b/fccf/build/_deps/json-src/single_include/nlohmann/json.hpp:16406: void nlohmann::detail::serializer<BasicJsonType>::dump(const BasicJsonType&, bool, bool, unsigned int, unsigned int) [with BasicJsonType = nlohmann::basic_json<>]: Assertion `false' failed.
    Aborted

But there is a bug, described in another md file. So that's not viable right now. 

Dump everything in standard format. Is that even realistic?

    $ time fccf --json . > everything.json
    real	0m15.423s
    user	1m9.241s
    sys	0m6.598s    

    $ wc -l everything.txt 
    322735 everything.txt

Yes it is. 

# What would I do with everything.json?

If I had gotten a json file with everything, then I could have inserted them into a database. 
And then I could write my own python app with a much better cli, that could search in that database. 

This was when I thought the biggest issue with fccf was the poor cli (not obvious how to use, and crashes in not so cool ways when used incorrectly), but now I see that it has other bugs too, that simply makes it crash. 
