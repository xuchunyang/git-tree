# `git-tree`

`git-tree` is a fork of the famous [`tree`](http://mama.indstate.edu/users/ice/tree/) command to respect `.gitignore`.

`tree` vs `git tree`:

    $ tree                                $ git tree
    .                                     .
    ├── CHANGES                           ├── CHANGES
    ├── INSTALL                           ├── INSTALL
    ├── LICENSE                           ├── LICENSE
    ├── Makefile                          ├── Makefile
    ├── README                            ├── README
    ├── README.md                         ├── README.md
    ├── TODO                              ├── TODO
    ├── color.c                           ├── color.c
    ├── color.o                           ├── doc
    ├── doc                               │   ├── tree.1
    │   ├── tree.1                        │   ├── tree.1.fr
    │   ├── tree.1.fr                     │   └── xml.dtd
    │   └── xml.dtd                       ├── hash.c
    ├── git-tree                          ├── html.c
    ├── hash.c                            ├── json.c
    ├── hash.o                            ├── strverscmp.c
    ├── html.c                            ├── tree.c
    ├── html.o                            ├── tree.h
    ├── json.c                            ├── unix.c
    ├── json.o                            └── xml.c
    ├── strverscmp.c
    ├── strverscmp.o                      1 directory, 19 files
    ├── tree.c
    ├── tree.h
    ├── tree.o
    ├── unix.c
    ├── unix.o
    ├── xml.c
    └── xml.o
    
    1 directory, 28 files

as you can see `*.o` and `git-tree` are not shown by `git tree`, because they are ignored by `.gitignore`.

## Install

[libgit2](https://libgit2.github.com/) is required, e.g., install it via Homebrew:

    $ brew info libgit2

then build `git-tree`:

    $ make git-tree

finally put it into your `PATH`, and you will be able to use it via `git tree` (or `git-tree`):

    $ mv git-tree ~/bin
