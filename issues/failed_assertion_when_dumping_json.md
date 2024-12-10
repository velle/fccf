This is the only error message I have seen that looks different from the rest. 

I tried to dump everything inside QGIS/src, to json. 

    ~/a/QGIS/src$ time fccf --json . > everything.json
    fccf: /home/velle/b/fccf/build/_deps/json-src/single_include/nlohmann/json.hpp:16406: void nlohmann::detail::serializer<BasicJsonType>::dump(const BasicJsonType&, bool, bool, unsigned int, unsigned int) [with BasicJsonType = nlohmann::basic_json<>]: Assertion `false' failed.
    Aborted

    real	0m15.011s
    user	1m7.581s
    sys	0m6.607s

So the code that throws the assertion is an external dependency. The assertion expression is simply `false`, so probably execution reached a point in the code that it was not supposed to. And the assertion provides no helpful explanation. 

Considering that fccf is not very mature and I found many other issues, the underlying issue is almost certainly 
in fccf. 

