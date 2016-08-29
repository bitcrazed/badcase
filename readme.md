# BadCase
Test project containing two files with the same name that differ only by case.

On Linux, only the file matching the requested case is opened. Accessing unmatched files return an error.

    $ cat hello.txt
    Hello, World
    $ cat Hello.txt
    BWAAHHHAHHAHAH
    $ cat HELLo.Txt
    cat: HELLo.Txt: No such file or directory

On Windows, the capitalized-case file is loaded, regardless of the case of the requested file.

    PS > cat .\Hello.txt
    BWAAHHHAHHAHAH
    PS > cat .\hello.txt
    BWAAHHHAHHAHAH
    PS > cat .\HELLo.Txt
    BWAAHHHAHHAHAH

Further, cloning this repo on Windows discards the Hello.txt file completely!
```
PS C:\dev> ls .\badcase2\


    Directory: C:\dev\badcase2


Mode                LastWriteTime         Length Name
----                -------------         ------ ----
-a----        8/29/2016     16:18             14 hello.txt
-a----        8/29/2016     16:18           1089 LICENSE
-a----        8/29/2016     16:18            590 readme.md
```

