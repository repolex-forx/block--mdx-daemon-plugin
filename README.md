# Repolex Knowledge Graph of block/mdx-daemon-plugin

RDF knowledge graph data for [block/mdx-daemon-plugin](https://github.com/block/mdx-daemon-plugin), parsed by [repolex](https://repolex.ai).

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
rlex download block/mdx-daemon-plugin
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 071e4b0b9d8d398e44647d6c4d9171b884e16328
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 071e4b0b9d8d398e44647d6c4d9171b884e16328
│           └── chunk-001.nq.gz
├── blob
│   ├── 01a17147e35bd5143e0a5bac39a5b1fbd35cb6bd.nq.gz
│   ├── 0600cd5edb5854a7f6a53caf8024fae7315718fd.nq.gz
│   ├── 0703f389efd7cd6b3b2017da389521309d4dce58.nq.gz
│   ├── 0750e9566a7c3d84cc26358dafd566eb059a9c90.nq.gz
│   ├── 08c578c05b3d1445ed3133132668cb7270625ebd.nq.gz
│   ├── 14f042dc863af97f7fb7bbfdceadb9728d70408a.nq.gz
│   ├── 15ea91d3622449bca244dd901b6c3a0afef48f92.nq.gz
│   ├── 1b6c787337ffb79f0e3cf8b1e9f00f680a959de1.nq.gz
│   ├── 2370d8bb4d48c6d16288957a696e9406460acdee.nq.gz
│   ├── 249e5832f090a2944b7473328c07c9755baa3196.nq.gz
│   ├── 272df666c327189d2705f949d70188ed452716ab.nq.gz
│   ├── 2733ed5dc3cd1ac040d18b9f10f8b806ce846704.nq.gz
│   ├── 2f552b95abf726ad0201caece3a255d7e9d5e99f.nq.gz
│   ├── 333a45c090bccc0a7f9b69ca8909010a07ff711d.nq.gz
│   ├── 35e1cdc5e9e1057cc9d2fea033c5e72e204ed646.nq.gz
│   ├── 3b1ec85c2b31aa2383d2bd35cb7db7e28d3393b2.nq.gz
│   ├── 40cca7357897c7bd67e111867bd723f27a7af10e.nq.gz
│   ├── 4252cbae3054d2bedaf8a74eb7e47349e0f7e25b.nq.gz
│   ├── 4d069410c2e964c4094be1545f55382847cd7444.nq.gz
│   ├── 4e1eadcba4dc43aa1e6e7639674678bd3df56e51.nq.gz
│   ├── 5b72975d3828628325f6a1685a143bc928a17e00.nq.gz
│   ├── 6bccf43368fd7c96d9c659562a5142b8b8cb98a1.nq.gz
│   ├── 6d37b056a70ab17915a2f36cfa5aa2ecd47e007a.nq.gz
│   ├── 6dbe89799101379853eaa544511f882bb3cfb6d0.nq.gz
│   ├── 7012b8a9417826a90ce49db7f7e0ba0206e4a09d.nq.gz
│   ├── 878905c05a67a8324647e69daf229b04f95cc30b.nq.gz
│   ├── 87fb12a1b9281af222e08382763e7ab1881c9ed9.nq.gz
│   ├── 8886e67aeafc5e666f939febb3fcf86f98b2b59a.nq.gz
│   ├── ac1b06f93825db68fb0c0b5150917f340eaa5d02.nq.gz
│   ├── cc37d538736a3c28ab5e0f848d4caa9947774c79.nq.gz
│   ├── dd5bc708be261d81713cade50721d5e10aa403ef.nq.gz
│   ├── e7f10e818d9b08eee98be3fee78e0ba6b2713d3f.nq.gz
│   ├── e9187d6f5705c871f90b94e92977427f39730ab9.nq.gz
│   └── f4c75dfa43cf6927ee85be39ea26d1ab53ffc67d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 071e4b0b9d8d398e44647d6c4d9171b884e16328.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 41 files
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

[block/mdx-daemon-plugin](https://github.com/block/mdx-daemon-plugin)

---
*Parsed on 2026-11-09 by [repolex](https://repolex.ai)*
