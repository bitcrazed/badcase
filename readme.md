# BadCase
Test project containing two files with the same name that differ only by case.

On Windows, capitalized-case file is loaded, regardless of the case of the requested file.

    PS > cat .\Hello.txt
    BWAAHHHAHHAHAH
    PS > cat .\hello.txt
    BWAAHHHAHHAHAH

On Linux, the file matching the requested case is opened.

    $ cat hello.txt
    Hello, World
    $ cat Hello.txt
    BWAAHHHAHHAHAH


