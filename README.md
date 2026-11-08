# Repolex Knowledge Graph of deepset-ai/dc-custom-component-template

RDF knowledge graph data for [deepset-ai/dc-custom-component-template](https://github.com/deepset-ai/dc-custom-component-template), parsed by [repolex](https://repolex.ai).

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
rlex download deepset-ai/dc-custom-component-template
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f94b192b785102af53ccdabeb15ee094d0437c2a
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── f94b192b785102af53ccdabeb15ee094d0437c2a
│           └── chunk-001.nq.gz
├── blob
│   ├── 0c03128cdb509de03bb02d3bcea2857c58470e67.nq.gz
│   ├── 3e0c9b6df243fdfbad59b2f69ebdf92821632455.nq.gz
│   ├── 720d6d5c7ccd5cb6d0e8257acbe3c454efb406ae.nq.gz
│   ├── 9f043604704ab12a42e36bc5dcf53b6af7c3a83b.nq.gz
│   ├── a5e32fac88e16fb2385eb2eb2a8b3109b67cd840.nq.gz
│   ├── b42ac3458d571119439831884fe331d8f78df4f2.nq.gz
│   ├── bfe70a8d38b25fdc6d29f16cb13fa4b8c28d4ca7.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f09caf4242d101ed90a3e93e6ac94334df863d6f.nq.gz
│   └── f3da7c21f2f0d737c318d48bd151a1cc8ada938a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── f94b192b785102af53ccdabeb15ee094d0437c2a.nq.gz
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

[deepset-ai/dc-custom-component-template](https://github.com/deepset-ai/dc-custom-component-template)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
