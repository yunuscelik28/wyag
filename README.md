# Wyag (Write Yourself a Git)

This is a custom implementation of Git built from scratch in Python. It was developed to deeply understand how Git works under the hood, including its object model, hashing, and index management.

## Acknowledgements
This project was built by following the excellent [Write yourself a Git!](https://wyag.thb.lt/) tutorial by Thibault Polge. All credit for the original architecture and learning material goes to the author. This repository serves as my personal implementation and learning milestone.

## Features Implemented
- **Repository Initialization:** `init`
- **Object Management:** `hash-object`, `cat-file`
- **Committing:** `add`, `commit`, `rm`
- **Tree and Log:** `ls-tree`, `log` (with Graphviz support)
- **Status & Ignore:** `status`, `check-ignore`
- **References:** `show-ref`, `tag`, `checkout`, `rev-parse`

## How it works
This project implements the core mechanics of Git:
- **Blobs:** Storing file contents compressed with zlib.
- **Trees:** Representing directories.
- **Commits:** Snapshots linking to a tree and parent commits.
- **Index (.git/index):** Managing staged files.

## Usage
You can use `wyag` just like you would use standard `git`:

```bash
python wyag init my_repo
cd my_repo
python ../wyag add <file>
python ../wyag commit -m "Initial commit"
python ../wyag log
```

*(Note: This is an educational project and lacks advanced networking features like `push`, `pull`, and `clone`, as well as `branch` merging/rebasing.)*
