Uutf — Non-blocking streaming Unicode codec for OCaml
-------------------------------------------------------------------------------
Release %%VERSION%%

Uutf is a non-blocking streaming codec to decode and encode the UTF-8,
UTF-16, UTF-16LE and UTF-16BE encoding schemes. It can efficiently
work character by character without blocking on IO. Decoders perform
character position tracking and support newline normalization.

Functions are also provided to fold over the characters of UTF encoded
OCaml string values and to directly encode characters in OCaml
Buffer.t values.

Uutf is made of a single, independent, module and distributed under
the BSD3 license.

Home page: http://erratique.ch/software/uutf  
Contact: Daniel Bünzli `<daniel.buenzl i@erratique.ch>`


## Installation

Uutf can be installed with `opam`:

    opam install uutf

If you don't use `opam` consult the [`opam`](opam) file for build
instructions and a complete specification of the dependencies.


## Documentation

The documentation and API reference is automatically generated by
`ocamldoc` from `uutf.mli`. It can be consulted [online][3] and there
is a generated version in the `doc` directory of the distribution.

[3]: http://erratique.ch/software/uutf/doc/Uutf


## Sample programs

Sample programs are located in the `test` directory of the
distribution. They can be built with:

    ocamlbuild -use-ocamlfind tests.otarget

The resulting binaries are in `_build/test` :

- `test.native` tests the library, nothing should fail.
- `utftrip.native`, among other things, reads unicode on `stdin` and rewrites 
  it on `stdout`. Invoke with `--help` for more information. Depends
  on [Cmdliner](http://erratique.ch/software/cmdliner).
