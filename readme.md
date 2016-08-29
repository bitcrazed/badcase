# BadCase
Test project containing two files with the same name that differ only by case.

On Windows, the capitalized-case file is loaded, regardless of the case of the requested file.

    PS > cat .\Hello.txt
    BWAAHHHAHHAHAH
    PS > cat .\hello.txt
    BWAAHHHAHHAHAH
    PS > cat .\HELLo.Txt
    BWAAHHHAHHAHAH

On Linux, only the file matching the requested case is opened. Accessing unmatched files return an error.

    $ cat hello.txt
    Hello, World
    $ cat Hello.txt
    BWAAHHHAHHAHAH
    $ cat HELLo.Txt
    cat: HELLo.Txt: No such file or directory

