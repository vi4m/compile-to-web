# Crystal Instructions

## Additional Installation

1.  install [Crystal](http://crystal-lang.org/docs/installation/index.html)
    (tested with version 0.17.4)

## llvm

``` sh
# compile to llvm ir
crystal build --emit=llvm-ir --single-module hello.cr
```

## asm.js - broken

``` sh
# compile to asm.js
emcc hello.ll
# run code
node a.out.js
```

## Web Assembly - broken

``` sh
# compile to llvm object
llc hello.ll -march=wasm32 -filetype=asm -o hello.s
# compile to web assembly
s2wasm hello.s > hello.wast
```
