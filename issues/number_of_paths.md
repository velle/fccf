The help message implies exactly one path. But in fact it can be left out, or you can enter several. If entering several paths, then it will traverse them all completely, even if they overlap. So some files may be searched twice, and results shown twice. 

velle@velle-ThinkPad-W530:~/a/QGIS/src$ fccf --enum '' | wc
   1264    3053   29005
velle@velle-ThinkPad-W530:~/a/QGIS/src$ fccf --enum '' . | wc
   1264    3053   29005
velle@velle-ThinkPad-W530:~/a/QGIS/src$ fccf --enum '' . . | wc
   2527    6106   58009