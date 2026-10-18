# Repolex Knowledge Graph of simonpercivall/astunparse

RDF knowledge graph data for [simonpercivall/astunparse](https://github.com/simonpercivall/astunparse), parsed by [repolex](https://repolex.ai).

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
rlex download simonpercivall/astunparse
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 2acce01fcdda2ea32eea835c30ccca21aaff7297
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 2acce01fcdda2ea32eea835c30ccca21aaff7297
│           └── chunk-001.nq.gz
├── blob
│   ├── 099193e44925fc67f3fba7fc946489c44ae6bb1c.nq.gz
│   ├── 0a8df87af1cba513e357c847bdd62decd5e35800.nq.gz
│   ├── 0ef6fd8bcbffa8fe6245246f13ed301bdcb9492c.nq.gz
│   ├── 1005e265973ba976766d336b6c043d066e663d6e.nq.gz
│   ├── 1729cd7c98a88f1afe19c89f996b78c6ec49c687.nq.gz
│   ├── 2b4476477fe314cdf9e221f94cecc0727f32d8c9.nq.gz
│   ├── 358a772099dbe3c93ca8bcf3145169008da4cb5f.nq.gz
│   ├── 3bdd7dc21ab8a25854b5fd89f2eeae8a3af657d6.nq.gz
│   ├── 43bed2addec330e2f2126ccbbdfa6b328affa8d3.nq.gz
│   ├── 5fa4e886b7b8583d2903cb62412a0bb14ba73cce.nq.gz
│   ├── 60e593971b94038a4f4344104b3405f56bd2e126.nq.gz
│   ├── 664b7348cae73ede6079eeb2da92e3fa5b8158a8.nq.gz
│   ├── 6da8b6ca888c75e5448c675d601ebcb72c14fdf3.nq.gz
│   ├── 6f33531a1b891b3d2e467d2dcb8bb4dddcea90bf.nq.gz
│   ├── 7043e86d08ce6adfad486288452b4e883ca67433.nq.gz
│   ├── 745b5694910d21879c6d3da486be61d9992ba43a.nq.gz
│   ├── 774bd7cfbd58b684e747a01d228c08e30812e0bb.nq.gz
│   ├── 7f0a4b8e47af34272d19a7f41ac3326f16592ab2.nq.gz
│   ├── 84df23baa9ecae248f87c108ab25808bb5900baa.nq.gz
│   ├── 92d64f772bff92956f71aa41b806f9f57d074d04.nq.gz
│   ├── 94292d017cf692423bca025d38aae6a7773a3936.nq.gz
│   ├── 95b9755a3839a12e21ceedf64d4d2d3fe9c2290c.nq.gz
│   ├── 9c9f1d6c133c654290457da3a3149a810cf748bd.nq.gz
│   ├── d751805e3e2baf91ee2a94eff5ecd8c3d8636c54.nq.gz
│   ├── dbad2da50018b20b9e8cf4be1668cfeef2d4c6cb.nq.gz
│   ├── e2eeddc88f079f90cdc1df9ac8e6ba3b62578639.nq.gz
│   ├── e5a277a3726b7596cf9cbadf87399c98bbcd4df5.nq.gz
│   ├── eaeb1572e7870a56532b6cf3a3e7f4883e1475e5.nq.gz
│   ├── f0683ed92dad0481cd13ea2e661e8e33e822d00d.nq.gz
│   ├── f6953b60b335551e4ae18b7c6a40a05ab00d5a25.nq.gz
│   ├── f7b293856909cb71e96505cb97e3f57eec1c5af3.nq.gz
│   └── faa18be5bbf7d6e25d05b85f3c2126e1c0d0bd32.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 2acce01fcdda2ea32eea835c30ccca21aaff7297.nq.gz
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

[simonpercivall/astunparse](https://github.com/simonpercivall/astunparse)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*
