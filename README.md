# Repolex Knowledge Graph of python-hyper/documentation

RDF knowledge graph data for [python-hyper/documentation](https://github.com/python-hyper/documentation), parsed by [repolex](https://repolex.ai).

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
rlex download python-hyper/documentation
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 64c346d5822c6ca9e8f0aa6636e678d650624343
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 64c346d5822c6ca9e8f0aa6636e678d650624343
│           └── chunk-001.nq.gz
├── blob
│   ├── 02e93f46ea98bccf4e5f98c83944b665fbba9937.nq.gz
│   ├── 04c9b4878306dcd95ba398c1f1d3a73e4a53329c.nq.gz
│   ├── 06f9dfb285c7a7e1dfccbf6e67f1ec9f59a8d201.nq.gz
│   ├── 1648276cfd677ab4eaff65f1d622e9212ffc67c2.nq.gz
│   ├── 1f24b377fb82846ec3d8b107df34e6fc56f88512.nq.gz
│   ├── 25cb25939d1640337513b76742d21d57a0620e95.nq.gz
│   ├── 25d499ce8d934324145df0a619a8f7c600946a38.nq.gz
│   ├── 4a4f054bad98dbbaa7fc6df0b5b49a3ef816c5b8.nq.gz
│   ├── 5d2ac333d4d0d4236c69d0ddba58bc44bd90fd1f.nq.gz
│   ├── 66acb384ece84a85664bc93d7554b3d6c8b6aff2.nq.gz
│   ├── 6a4c92809b9535d438d94a9865fdcaa654733e22.nq.gz
│   ├── 6afe806357bfda9a745b5305b84aa43b51c0a53d.nq.gz
│   ├── 6e757894b00b4a27a1c5ba5b5fd562ef7a600c1f.nq.gz
│   ├── 870a94b8b0fb9ec4eff4f894a98179ffbbc037eb.nq.gz
│   ├── 9f2ac6009b94861b126b2c68a0a0ad72ac32587f.nq.gz
│   ├── 9f5594e8ebd6d49c3efc6a1e7fb6f6e57b2b2be6.nq.gz
│   ├── baca6bdf07263018b86ed01c1d99f2c86cec8b64.nq.gz
│   ├── d6466b602473a2683ccf84a9f6c6dce140a058e3.nq.gz
│   ├── d6745675b310ad0bf921e470b9c1dff0fa12da5a.nq.gz
│   ├── eb505264469499a647f080c1d991deb46222fdb6.nq.gz
│   ├── f075daf8f4ff4604bebe99e06b92bbbee584b18a.nq.gz
│   ├── f59e24a09efecb05e3480b94bce73ae73b303ea1.nq.gz
│   ├── f86fac90c2594632d05d3029208b50b85e1643e7.nq.gz
│   └── fdcfadeb0cecaaccb13c7700f5043cebadbba394.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 64c346d5822c6ca9e8f0aa6636e678d650624343.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 32 files
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

[python-hyper/documentation](https://github.com/python-hyper/documentation)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
