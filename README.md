# Repolex Knowledge Graph of jupyterlab/jupyterlab_pygments

RDF knowledge graph data for [jupyterlab/jupyterlab_pygments](https://github.com/jupyterlab/jupyterlab_pygments), parsed by [repolex](https://repolex.ai).

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
rlex download jupyterlab/jupyterlab_pygments
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c3380f5c973c74e13f7832504749d6ec11c5f491
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── c3380f5c973c74e13f7832504749d6ec11c5f491
│           └── chunk-001.nq.gz
├── blob
│   ├── 06d298c6e2a0181c515edf2867f266581247d4cd.nq.gz
│   ├── 0802975fc27119c4af58acf6e0323e213f00d8de.nq.gz
│   ├── 20131a028bafd8e98ad129c84810c38ceedb7c85.nq.gz
│   ├── 2c41d3c4cfc8a288acf7de733690402ae71a649b.nq.gz
│   ├── 2d352af421a2a63c8264e83877f79497337429a6.nq.gz
│   ├── 38b2628e4f88898dea48c5feb2cf4872c10a0d61.nq.gz
│   ├── 3c53eaf5ae3431efe8b47826218ce2963917d7a3.nq.gz
│   ├── 48a06303d247e9506b39112587e0277978bf4995.nq.gz
│   ├── 51384b133ac4297465419f936f4f07f69765b1e7.nq.gz
│   ├── 6e888676996d26f4315181819c6990a60eb1bc8d.nq.gz
│   ├── 725feab5ce652dc39f3f2c77b9fd3c90bf049c65.nq.gz
│   ├── 87e9cd29b58fdb1d83807bac61659dbaf58e1370.nq.gz
│   ├── 8a2e3cb75114d4ee175912cf868ed278ffabaf9e.nq.gz
│   ├── 8a7ea29e69487a93c256fee6e15adfd533a53280.nq.gz
│   ├── 98979175c601f76021be67e181e30b3950d090c0.nq.gz
│   ├── 98cf07cbdae6b406825140c237d5deb1a77ccb88.nq.gz
│   ├── 9b0ef359a65ac9d6a7f43a692d932ae63bee2673.nq.gz
│   ├── a028a76408bf46181259249b2e15e14a9bbdf7f1.nq.gz
│   ├── aefdf20dbcd4c5c7b8bc90a83f19e845d6da6b64.nq.gz
│   ├── b21c51a6d4bdfded0dea2f1ea68c4a3283f2de13.nq.gz
│   ├── bbdd198a0153b7496fc8a7970e13c99e518151cc.nq.gz
│   ├── c897932c8cee13f1bc7b26212edb31d9efa90d81.nq.gz
│   ├── cca6a5aea2b51f7853bf5b9a7a17cb9a2ff93a25.nq.gz
│   ├── d1b04671d9698ef1b9e629f3c1f67d5cc26a6679.nq.gz
│   ├── d882c1c9d1452ad0d4021b5455ff083686e53aa1.nq.gz
│   ├── deb2c38c8ecf6a0a88e5ad8cfdd42625dab32d05.nq.gz
│   ├── e0cdfaa4e61f1ca4038c540ad97f3b50504f7774.nq.gz
│   ├── eb933ab7f0468ffe6379e985fc2e1bfc98652c4a.nq.gz
│   ├── ecb9ba8d6b469dfdd3fecd71754332e9d101771e.nq.gz
│   ├── ee3b3e2228afa33f083acba25542dd9986d214bb.nq.gz
│   └── f12ec7f15d95094dcf3a4451493b2202511e8507.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c3380f5c973c74e13f7832504749d6ec11c5f491.nq.gz
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

[jupyterlab/jupyterlab_pygments](https://github.com/jupyterlab/jupyterlab_pygments)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
