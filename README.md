# Repolex Knowledge Graph of pypa/setuptools-issue-900

RDF knowledge graph data for [pypa/setuptools-issue-900](https://github.com/pypa/setuptools-issue-900), parsed by [repolex](https://repolex.ai).

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
rlex download pypa/setuptools-issue-900
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 4025ff7c93ccc0bcba35c40ba03e9db3acfaed83
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 4025ff7c93ccc0bcba35c40ba03e9db3acfaed83
│           └── chunk-001.nq.gz
├── blob
│   ├── 01ff14dab1ceb0d94e2af607ec3445a85e8a47b4.nq.gz
│   ├── 4697696295af902f3a30e789a5fd5961920f7a09.nq.gz
│   ├── 658b2163fb6dc07c569211feb48e85416a6cf12c.nq.gz
│   ├── 7c60020200f2211dd63aae64a97a58e5477438eb.nq.gz
│   ├── 9cc0939836ee0fa92b0b680592135aa56fcd5e2c.nq.gz
│   ├── a2056e5e2f176b6508aa7346e4601e24c6eac112.nq.gz
│   ├── d9f142371748b2e22e59e768da19c69919ce859b.nq.gz
│   ├── de40ea7ca058e07a399acf61529d418c07eeee61.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 4025ff7c93ccc0bcba35c40ba03e9db3acfaed83.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 15 files
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

[pypa/setuptools-issue-900](https://github.com/pypa/setuptools-issue-900)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
