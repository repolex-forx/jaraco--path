# Repolex Knowledge Graph of jaraco/path

RDF knowledge graph data for [jaraco/path](https://github.com/jaraco/path), parsed by [repolex](https://repolex.ai).

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
rlex download jaraco/path
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── b5ae11e41ba64a9e27fdc42d8c138d7db7699910
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── b5ae11e41ba64a9e27fdc42d8c138d7db7699910
│           └── chunk-001.nq.gz
├── blob
│   ├── 0090b624cdf09b1a21d302ff16542b13c202bced.nq.gz
│   ├── 0a5a245f8391d0b97d2b0ab9a3ffdaadb4152403.nq.gz
│   ├── 150d9358269b525147a81c1b8c7eeaa015b61699.nq.gz
│   ├── 172bf5786d1a8805816c0936413c8ee1c1bdf6ed.nq.gz
│   ├── 1f2aa7533b0423a8eb943f6f4ec02498e39581a0.nq.gz
│   ├── 23ca48d8ff44077121350c8b5f885b5ae16619b8.nq.gz
│   ├── 304196f81e11a168c9894f966e4a617ebf4ed53c.nq.gz
│   ├── 54c9000ec94341dd65c2053251b85b124017b9b5.nq.gz
│   ├── 54cc8303b22089e12053e552d4e6cb852a865b8a.nq.gz
│   ├── 54f99acbfac68c2be8283174ea64f1730a795e49.nq.gz
│   ├── 55d733cf2e2b12f3a5932835724fcb2a2e60da17.nq.gz
│   ├── 577e87a793a20e413f7321f4f17ec1eba2ea1962.nq.gz
│   ├── 5c05f9e27d57a4b7a3c3a9fdfecf8cddb8be499f.nq.gz
│   ├── 5dd08896051dd273045c78fc5c70932389c6e9d7.nq.gz
│   ├── 700235be57c1b2872455c0be5333f59cf568e252.nq.gz
│   ├── 724370638fc188317bbc7dc868f1a571995fd796.nq.gz
│   ├── 731e88ec9c5b1e9ecdf2dd931f660cd6eb3e4fed.nq.gz
│   ├── 8a0ce607e89b13a7a72fc0a94781ffbcdb2f0a93.nq.gz
│   ├── 93e57e9a86e4cb79a6c798398b53c4b9b6558c57.nq.gz
│   ├── 9a0f3bce1395ae3819030b822e5d9076c85068ea.nq.gz
│   ├── a6ab591f5d8fe7167ece948405e8049a977f252e.nq.gz
│   ├── b4a10ac96afc7c49a9c877072c6265d075820183.nq.gz
│   ├── bdac15317e07bbb699e37c2ac008b529e38e86bf.nq.gz
│   ├── d7fadafa23493c51ad0ff4896432ffb6ea703a01.nq.gz
│   ├── e05a3d4a2ab888e32952006d8cd380864368db5f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── eab7315ba2f38516729b82419e701c6249ee8777.nq.gz
│   ├── eb6c76532a801faa3d99023052c87f949207f6a6.nq.gz
│   ├── efcb8cbc2043faa7caf4f92fc7488bd6914c934c.nq.gz
│   ├── f880c90c1f80e1a4e1d7c46ad6c053c2ca063b9c.nq.gz
│   ├── fdea1552a4a13487e5d9d08733ffb3a62969f471.nq.gz
│   └── fe85d77bd9e8cdd9f9eb439d8da057a8fbe278d6.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── b5ae11e41ba64a9e27fdc42d8c138d7db7699910.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 40 files
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

[jaraco/path](https://github.com/jaraco/path)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*
