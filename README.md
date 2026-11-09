# Repolex Knowledge Graph of ReVanced/revanced-patches-template

RDF knowledge graph data for [ReVanced/revanced-patches-template](https://github.com/ReVanced/revanced-patches-template), parsed by [repolex](https://repolex.ai).

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
rlex download ReVanced/revanced-patches-template
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── bd4b564fc0fc8f7ade8dcd41eb4aaaf59adad6ae
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── bd4b564fc0fc8f7ade8dcd41eb4aaaf59adad6ae
│           └── chunk-001.nq.gz
├── blob
│   ├── 03f8580adae9578ad2b8c5607aed4104cdc7ff7e.nq.gz
│   ├── 0936e28e511260ae3126804110e8aed0029a33a6.nq.gz
│   ├── 097f9f98d9eec50af4ab357b4913aa9bf5a12b0e.nq.gz
│   ├── 15f02e678aa7cdd8a2c1079bae41580187fb54b7.nq.gz
│   ├── 19eb00e819819945bc41195eba118876fe75fa8b.nq.gz
│   ├── 277dc5b33707b315e3c9f542f430f3853eed8ea2.nq.gz
│   ├── 2c3521197d7c4586c843d1d3e9090525f1898cde.nq.gz
│   ├── 2d6d258f47baddb6432e9c5e59a7997b18f6a78d.nq.gz
│   ├── 3c5eeccc70e6ffb3dbac1898d1f14333f82994be.nq.gz
│   ├── 3c6228a09442e1258ad8d3fa35354ad4746d2111.nq.gz
│   ├── 4729d416db8bb5011ff77d995c67619a868684c0.nq.gz
│   ├── 536b6614a783bf8d6023757123fd31d492573044.nq.gz
│   ├── 68e8816d71c98108f09712e252a7df785202e889.nq.gz
│   ├── 75b8e67fa325d925ae9c66457e0edb8c08258fca.nq.gz
│   ├── 815817352125a1b57db831f3b7a506b839b1fbd2.nq.gz
│   ├── 83c1a310ff860dc48e0e9a64c2c01938922fad86.nq.gz
│   ├── 87ebc124435b104ccf5da515a243eee3bdd0fe25.nq.gz
│   ├── 901e1914b4182fc2695ff8749e824619460e1fff.nq.gz
│   ├── 93e7caf35d170446e77030ba2c6636001019b7d0.nq.gz
│   ├── 979a816ac286870356980265d5bd65c398d6c80e.nq.gz
│   ├── 99ebf79a22452e025bdbe02a5c6ac842ac0ae5a6.nq.gz
│   ├── 9b65eb06cff68464b3002060558a2ffb482f343c.nq.gz
│   ├── 9d21a21834d5195c278ba17baec3115b2aaab06e.nq.gz
│   ├── a59bfb50bfdff7c1e5bb9a408ebbfb4de1badb30.nq.gz
│   ├── bbc4fd513d1e0ac18b51d29bbf8a5bfab17183c6.nq.gz
│   ├── beb08f2b92fce3e5c31dfbda58c2348441c2037e.nq.gz
│   ├── c9bf68b05d904b61a20527955d2516df02ac738f.nq.gz
│   ├── d486cc964e0367063907aec8ccff386ba9fda6fa.nq.gz
│   ├── f288702d2fa16d3cdf0035b15a9fcbc552cd88e7.nq.gz
│   ├── f404582d2817cba0a731510a6a6eb79ee2a65896.nq.gz
│   └── f5feea6d6b116baaca5a2642d4d9fa1f47d574a7.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── bd4b564fc0fc8f7ade8dcd41eb4aaaf59adad6ae.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 39 files
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

[ReVanced/revanced-patches-template](https://github.com/ReVanced/revanced-patches-template)

---
*Parsed on 2026-11-09 by [repolex](https://repolex.ai)*
