ogzip
=====
Portable OpenBSD `gzip` utility.

Can use either your system's zlib or the included miniz.

Why?
----
Why not? Some people like that minimalist and/or static linking aesthetic.

Supported platforms
-------------------
Probably anything that has a working C99 compiler.
Pull Requests to add additional platform support always welcome.

Supported compilers
-------------------
`ogzip` is known to build with the following C compilers:
* [clang](https://llvm.org/)
* [gcc](https://gcc.gnu.org/)
* [pcc](https://pcc.ludd.ltu.se/)
* [Tiny C Compiler](https://bellard.org/tcc/)
* [cparser](https://pp.ipd.kit.edu/firm/)
* [lacc](https://github.com/larmel/lacc)
* [cproc](https://sr.ht/~mcf/cproc/)
* [vbcc](http://www.compilers.de/vbcc.html)
* [Nils Weller's C compiler](https://nwcc.sourceforge.net/)

Building with a compiler not listed here? Add it and send a pull request!

Building
--------
Run the `configure` script, then run `make`.

An important tip is to add the `--enable-lto` flag if you use
`--enable-miniz` as LTO can reduce the final binary size by up to 10 KB.

License
-------
The OpenBSD parts are BSD and ISC licensed.
The miniz library is MIT licensed.
