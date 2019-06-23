## Working with native ReasonML

For working with native ReasonML, the 2 tools I've found to be useful are:

1) `dune`, for building packages, integrates opam packages as long as they're properly referenced, and
2) `esy`, for installing both npm and opam packages needed by the native ReasonML project (also permits you to make configs for building your project in the `package.json` file).

### Dune

See `Makefile` in project root for sample commands. This project uses an opam installed `ocaml-csv` package, which is then referenced in the `dune` file in root (`ocaml-csv` is just used to demonstrate how to integrate an opam-installed package). 
You can also create as many of your own libraries in subdirectories as you want, and reference them in the same way as opam-installed packages are referenced in the `dune` config file.

Some docs on dune:

* https://dune.readthedocs.io/en/latest/quick-start.html (general docs, with examples in OCaml)
* https://til.hashrocket.com/posts/qljaabp1yb-compile-reasonml-to-native-with-dune (shows example in ReasonML, dune compiles native ReasonML with zero additional configurations besides the ones needed for OCaml)

### Esy

https://esy.sh/en/

I didn't actually set up `esy` in this repo, but if you need to use packages from both opam and npm, esy looks like a good option.
