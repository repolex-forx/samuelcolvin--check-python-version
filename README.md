# Repolex Knowledge Graph of samuelcolvin/check-python-version

RDF knowledge graph data for [samuelcolvin/check-python-version](https://github.com/samuelcolvin/check-python-version), parsed by [repolex](https://repolex.ai).

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
rlex download samuelcolvin/check-python-version
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── db74af5ee0b4535d185361599f8a3452f19cb3d2
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── db74af5ee0b4535d185361599f8a3452f19cb3d2
│           └── chunk-001.nq.gz
├── blob
│   ├── 05a14c3b7aac63c7ecaa1b64332f51edf8147a9c.nq.gz
│   ├── 0a699988e939d818eb3040c260e51c0863eec8fc.nq.gz
│   ├── 2a633a38c68d5fc76410561722224035117fbd88.nq.gz
│   ├── 45e559fbe6d19e8bdfdc3d00304f4dd6bdaeb45c.nq.gz
│   ├── 6550b665ca3f7f1411f34b65cb2f2e99e729c4bf.nq.gz
│   ├── 6c62ee45048f69d2ad078f5b7732276f5746cdba.nq.gz
│   ├── b69c9dfe2150825091888d62d791c567262eba58.nq.gz
│   ├── d9911b3ae14115a234f2e862b528bd62b98888a5.nq.gz
│   ├── e2b8c1032cfd49eb9b167150d17b75fda33936ac.nq.gz
│   └── f5ddc1a1bce67c9b73a15c2fdc25469e30b546cf.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── db74af5ee0b4535d185361599f8a3452f19cb3d2.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 18 files
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

[samuelcolvin/check-python-version](https://github.com/samuelcolvin/check-python-version)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
