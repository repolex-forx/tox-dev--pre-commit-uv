# Repolex Knowledge Graph of tox-dev/pre-commit-uv

RDF knowledge graph data for [tox-dev/pre-commit-uv](https://github.com/tox-dev/pre-commit-uv), parsed by [repolex](https://repolex.ai).

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
rlex download tox-dev/pre-commit-uv
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── edc4fbece3f125badeacbdae8eb80df3d437ccd5
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── edc4fbece3f125badeacbdae8eb80df3d437ccd5
│           └── chunk-001.nq.gz
├── blob
│   ├── 10e740e9f7957eda52d55a88e3dafb2521a260ce.nq.gz
│   ├── 267eaab0147a24207d2efe59cefb25db1bc288f1.nq.gz
│   ├── 3213fcc33e0fc5bd478ac69dfa250bed60b3a184.nq.gz
│   ├── 364982344fbd94d55705e1f27a9a87abaa255333.nq.gz
│   ├── 4f7a66be8a14993367dd88397fac0716664885c1.nq.gz
│   ├── 5f89818f9e63c2f6829c7706c57f223cdb5bbd38.nq.gz
│   ├── 6034a7e0a43f2697daefdf26b4d7601bdcfb58e3.nq.gz
│   ├── 64b8a3ced3e5deb9b4e47509e44324bf247f64be.nq.gz
│   ├── 785b7973980b9540f47e915bfe01717c317b6f1d.nq.gz
│   ├── 7f7d378c1cb6ce544964c747bb2bdb77ff8b8014.nq.gz
│   ├── 83b7aca26127590b0679803b38a07aca09f31791.nq.gz
│   ├── 866977d1c5cb0beacad179099f95182fa140bf75.nq.gz
│   ├── b89fdfaa258e2ce886cb45df2f732901139cfc5c.nq.gz
│   ├── be9c7d2e5dae5e5bac3ec412c594d1666e645f99.nq.gz
│   ├── d811f7fdbfbfa2d0044cb08e7597e1c4f9e6dda7.nq.gz
│   ├── e08736fa77f59c3dd65681c03d83de8bbf267150.nq.gz
│   ├── e5689eec1df675539f40b30250daf17eeab47a64.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── f6d7b5492feb9fa26e42b4ed6a11f6a8e88f675b.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── edc4fbece3f125badeacbdae8eb80df3d437ccd5.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 27 files
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

[tox-dev/pre-commit-uv](https://github.com/tox-dev/pre-commit-uv)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
