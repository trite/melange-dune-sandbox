# melange-dune-sandbox
Opam setup:
```
$ opam install reason dune melange mel ocaml-lsp-server
```

# Aliasing seems to generate .js files
```
$ cd basic-setup-with-alias/
$ dune build @app
$ cd _build/
$ pwd
/home/trite/git/melange-dune-sandbox/basic-setup-with-alias/_build
$ tree
.
├── default
│   ├── HelloOcaml.ml
│   ├── HelloReason.re
│   ├── HelloReason.re.ml
│   └── output
│       ├── HelloOcaml.js
│       └── HelloReason.js
└── log

2 directories, 6 files
```

# Without aliasing it seems like something goes wrong
```
$ cd basic-setup-without-alias/
$ dune build
$ cd _build/
$ pwd
/home/trite/git/melange-dune-sandbox/basic-setup-without-alias/_build
$ tree
.
├── default
│   ├── HelloReason.re
│   └── HelloReason.re.ml
└── log

1 directory, 3 files
```