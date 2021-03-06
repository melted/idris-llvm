# idris-llvm

This is a LLVM backend for Idris.

## Installing

Idris-llvm uses llvm-hs to bind to LLVM, it requires that a recent LLVM (at the moment LLVM 4.0) is installed in a location that GHC knows about. Required C libraries are the Boehm GC (it could be called "libgc" or "gc") and GMP.

If the prerequisites are met `cabal install` should be sufficient to build and install idris-llvm.

## Usage

There needs to be a clang executable available to build the programs. gcc will not work as the input files to clang are LLVM files.

How to build an executable:
```
idris myprog.idr --codegen llvm -o myprog
```