PAC-man
===============

Getting started
---------------
First you must initialize a repository with our sources:

    repo init -u git://github.com/PAC-man/android.git -b cm-10.2

Then sync it up (This will take a while, so get a cup of coffee and some snickers):

    repo sync


Building P.A.C
------------------------

For building P.A.C you must cd to the working directory.
Make sure you have your device tree sources, located on

    cd device/-manufacturer-/-device-

Now you can run our build script:

    ./build-pac.sh -device-

example:
    ./build-pac.sh urushi

You can also use a second parameter for syncing sources before building

    ./build-pac.sh -device- true


There are also a few parameters that you can use together with before mentioned:

* threads: Allows to choose a number of threads for syncing operation
* clean: Removes intermediates and output files

The usage is the same
    
    ./build-pac.sh -device- -parameters- true


Parameters will be considered false unless you set them to true

This will make a signed zip located on out/target/product/-device-.
