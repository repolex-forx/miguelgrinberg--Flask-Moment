# Repolex Knowledge Graph of miguelgrinberg/Flask-Moment

RDF knowledge graph data for [miguelgrinberg/Flask-Moment](https://github.com/miguelgrinberg/Flask-Moment), parsed by [repolex](https://repolex.ai).

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
rlex download miguelgrinberg/Flask-Moment
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── ec32737fbcb56dfec3412f51ee82598a808ba059
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── ec32737fbcb56dfec3412f51ee82598a808ba059
│           └── chunk-001.nq.gz
├── blob
│   ├── 07c392100ab95825a9fc02e4dbf28697d2c60137.nq.gz
│   ├── 10dd5123f09ac5e739bbc1f760ce5d6b798a83e5.nq.gz
│   ├── 182374c362dcde5f8916bd4da4920e0c5ea71607.nq.gz
│   ├── 1937f5425217026902010376ced39f40dfeea141.nq.gz
│   ├── 1cc59730baeb7333c301b85596c3087ff8457aa9.nq.gz
│   ├── 2008c81b26d8c79c089f3b632ee6e11053121186.nq.gz
│   ├── 2119f51099bf37e4fdb6071dce9f451ea44c62dd.nq.gz
│   ├── 2448fd2665df720101cf6662b17bfdfbda3e7cc3.nq.gz
│   ├── 250f570e6e94706459402810dd05090ea476a264.nq.gz
│   ├── 318643fd06894d8215512b3c1dbbbece580a3e6f.nq.gz
│   ├── 6239577c663af635a72b7d38b1787635f5795a30.nq.gz
│   ├── 66a04d95906cf4dd5128ee3bf8784cb72d39e40f.nq.gz
│   ├── 68b461a564bb5f466ec264a5361404e0540da716.nq.gz
│   ├── 810253c705df9250ceb479c0e5e10cb0e3e7524b.nq.gz
│   ├── 828c8cd3cbfd70000af584ae6a2ded4000289e1a.nq.gz
│   ├── a285e783bb12b71c91b87998e6bd26aa02796834.nq.gz
│   ├── ad436380f51638f10fca804c6feb78789afd4862.nq.gz
│   ├── b323a54046a4b1176853acc7b6d338eba748cf73.nq.gz
│   ├── b7cbd4f83de0b2907a227e80cbc4fd99e336f0dc.nq.gz
│   ├── c16529566da995c339667516913393cbaed97537.nq.gz
│   ├── d4bb2cbb9eddb1bb1b4f366623044af8e4830919.nq.gz
│   ├── d908aa79eaab6180d434cb0498e8252573b05c8e.nq.gz
│   ├── f8cbbb5e9d44739c204dff88257788d84c5b6a2c.nq.gz
│   └── fd099e2ea894afcdbe98a2e104cbaa1b37810158.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── ec32737fbcb56dfec3412f51ee82598a808ba059.nq.gz
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

[miguelgrinberg/Flask-Moment](https://github.com/miguelgrinberg/Flask-Moment)

---
*Parsed on 2026-10-19 by [repolex](https://repolex.ai)*
