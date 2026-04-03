# Repolex Knowledge Graph of asimov-platform/asimov-dataset-cli

RDF knowledge graph data for [asimov-platform/asimov-dataset-cli](https://github.com/asimov-platform/asimov-dataset-cli), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download asimov-platform/asimov-dataset-cli
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── blob
│   ├── 0460c360be29ce8e7197a3cb8c6aed4fa0114aca.nq.gz
│   ├── 0d29b413d3a30a3012cc627862195caea84ea5e1.nq.gz
│   ├── 1109dd81a65380c9ce2f9f7a6ba33ba54ab0908b.nq.gz
│   ├── 13edb27f8341a15f7ef6805243c5be8572913129.nq.gz
│   ├── 2391f73aa051d3804285ce744f2e9a1c7e08993d.nq.gz
│   ├── 2f05b805fe01c0c0304ac3848f358e54996cc9cb.nq.gz
│   ├── 3c5909464b6b81f3cefc3ab396072726a7d0c0c9.nq.gz
│   ├── 51e7bdc94e090c1e124270c5b99a3418c90a221e.nq.gz
│   ├── 52e80a16a2160d56a1ce6ca20132170e194aa074.nq.gz
│   ├── 70b50f72a723fd5825b898131b2db43e718d6b18.nq.gz
│   ├── 8b85e1998da7b980fd6e73025499443c58d9f113.nq.gz
│   ├── 90224374528012efa13e33e258e8f4333f1a9aab.nq.gz
│   ├── a444ba86bfb222f38f3578b3394460b8c053b574.nq.gz
│   ├── a718674ce58c2cb835775828c8a323d259c0848c.nq.gz
│   ├── bd70f4e6bf4795d664b4c9a73f8cd4f6231048fa.nq.gz
│   ├── c7504b17b600cacd0a72d17b05bb8dae214c4791.nq.gz
│   ├── d0bf8d9748f1e5c6b61f9f0134ab6bf524148831.nq.gz
│   ├── d2d774d685a805fac62723c16262a6ba9ded7549.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── ec50a64ded33981836d5e4a10ec60f3501f1ce74.nq.gz
│   ├── ed11761146321eaea9c993d36dd3b51bb5ea5193.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   ├── f4d9f07ab7fdeda19eca17a78b232c1cb4d96232.nq.gz
│   └── fd0ea036c4b73cd5f5421d9be4430e857556b1b0.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 8865d1a1777c326ccbdceff48f701223431cec1f.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

8 directories, 30 files
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

## Source repository

[asimov-platform/asimov-dataset-cli](https://github.com/asimov-platform/asimov-dataset-cli)

---
*Parsed on 2026-04-03 by [repolex](https://repolex.ai)*
