# Repolex Knowledge Graph of google-deepmind/dm_hard_eight

RDF knowledge graph data for [google-deepmind/dm_hard_eight](https://github.com/google-deepmind/dm_hard_eight), parsed by [repolex](https://repolex.ai).

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
rlex download google-deepmind/dm_hard_eight
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9e58b6f01d14d874bff16e8f9a2bb2b81c0f7b8d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 9e58b6f01d14d874bff16e8f9a2bb2b81c0f7b8d
│           └── chunk-001.nq.gz
├── blob
│   ├── 0dc5f7b406d6e70b65b4855014a9b3e097ec8422.nq.gz
│   ├── 1d3325f48ce7bd35fef75083091d2c2670581482.nq.gz
│   ├── 5406c20fdd9f607e5b2fa803055408551003c6c5.nq.gz
│   ├── 63cedb854d15eae284e1cb565c721bef5cc374bd.nq.gz
│   ├── 71182b78d4a4480641bb8859e186e52c8d110f71.nq.gz
│   ├── 7336d3b6e6edf63b8865bc5c074e35c4992c832f.nq.gz
│   ├── 878115b52af2f5cee93119086bb1ba977aab4b62.nq.gz
│   ├── 950146346d8243b46790c079cab62ccf9647aa5c.nq.gz
│   ├── 9a86ba025d83dfc39db62d84ee7cac0a9da1ac08.nq.gz
│   ├── 9f4f7cae1ff3740966b71745a5437cd474415d44.nq.gz
│   ├── b76b197f094b0bc1bb69bdb26e287177612b9167.nq.gz
│   ├── c5ed389b623fca601c800666fac36a256c974aff.nq.gz
│   └── d645695673349e3947e8e5ae42332d0ac3164cd7.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 9e58b6f01d14d874bff16e8f9a2bb2b81c0f7b8d.nq.gz
├── issue
│   └── issue.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 20 files
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

[google-deepmind/dm_hard_eight](https://github.com/google-deepmind/dm_hard_eight)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
