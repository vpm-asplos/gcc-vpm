GCC with VPM support
=====================

Currently, we only support GCC with VPM for the first stage.
This goal of this repository is to build the binary `cc1`, which compiles source code into `.s` assembly file.

## Building instructions

To build `cc1`, after running `git clone`, run the following commands.

```sh
./contrib/download_prerequisites
git submodule init
git submodule update
mkdir bld/ && cd bld
ln -s ../libfs .
../configure --enable-languages=c --disable-checking --disable-bootstrap --disable-multilib
make
```

You will find the `cc1` binary in `bld/gcc/` folder

