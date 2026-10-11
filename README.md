# Repolex Knowledge Graph of agronholm/reorder_python_imports

RDF knowledge graph data for [agronholm/reorder_python_imports](https://github.com/agronholm/reorder_python_imports), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download agronholm/reorder_python_imports
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── b34a28239d3abbe4f9523fe92409a0497f6ba97c
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── b34a28239d3abbe4f9523fe92409a0497f6ba97c
│           └── chunk-001.nq.gz
├── blob
│   ├── 094634f5d9ea2d1aeb611600a6a54cd341275cf6.nq.gz
│   ├── 0c5a37eb0adeb312718e533d0a4fbcbea6880056.nq.gz
│   ├── 194cee7975a10afde030c3d274af25941bf286b8.nq.gz
│   ├── 3d93aefb2da505dba9c0114404cfaaeee5ad0d3f.nq.gz
│   ├── 5a469fcafafb4da44f188c2862be06e1c664cb7e.nq.gz
│   ├── 5b9f17d8e0271b72057a8d1e53f15462e5655149.nq.gz
│   ├── 5e69924426da1020fe47ab6f5e9245e02d285800.nq.gz
│   ├── 5f66e9f5aef6ff8b70bfb4025e930540a2f72694.nq.gz
│   ├── 5ff1587f6d3bb0490d253b32500c90a75d9aeb18.nq.gz
│   ├── 642390e2ba5845a7262a2861b380f17c965d5616.nq.gz
│   ├── 6576c8b22ad99475344242f8886d5931cc54259f.nq.gz
│   ├── ada0df88fdb5e774b243160cb54dd9647fb29a0f.nq.gz
│   ├── c98d60c989a91ee5e3105ab2bfac8de6d2de480d.nq.gz
│   ├── d4c0d60a56ff111a4f37c0395fd3d9e57aad5795.nq.gz
│   ├── d7c0b8589a311bd47f9db1eb204c6dc109b11060.nq.gz
│   ├── d86d9ea06347dbd79c04079484155ea94fa2c3ed.nq.gz
│   ├── d99da5fd7036fa70cffd560d4a15c049c68770a8.nq.gz
│   ├── dc5942ed876ebca286861fed6ea3199b57aaf60f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── eabcf07976c9993887d70922998ba3791a71674f.nq.gz
│   └── ef399e07c9da934ed03bbdf696f373c086102f57.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── b34a28239d3abbe4f9523fe92409a0497f6ba97c.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 27 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[agronholm/reorder_python_imports](https://github.com/agronholm/reorder_python_imports)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
