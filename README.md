# Repolex Knowledge Graph of ansible-community/antsibull-tool

RDF knowledge graph data for [ansible-community/antsibull-tool](https://github.com/ansible-community/antsibull-tool), parsed by [repolex](https://repolex.ai).

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
rlex download ansible-community/antsibull-tool
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── bad7f03f9c3ac3f98915a6c9751543264da03773
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── bad7f03f9c3ac3f98915a6c9751543264da03773
│           └── chunk-001.nq.gz
├── blob
│   ├── 01077629ddb21821c86235b724c3622aae296875.nq.gz
│   ├── 01475b0c75a9bc027eb3db124fcdb9cbd9ec5e32.nq.gz
│   ├── 07b847ea5a8714732769a515ad0874dfb74caea9.nq.gz
│   ├── 0d0883f3454d5b18979658fb0231e00dace192a5.nq.gz
│   ├── 0e619bd88a03e972455f652482f966b7ca7028e9.nq.gz
│   ├── 3f2df240e2d8324f3eabd9dcb880992beaf3d63b.nq.gz
│   ├── 4c43c9b68c851ca401cd16ce58e0a409ea03d945.nq.gz
│   ├── 4f0ff17a0ade30f28b3f3d2d36d8bb48a162400f.nq.gz
│   ├── 50804672e0269f4e8b8d20cfc9ad7a1237607c31.nq.gz
│   ├── 52337f7b73697fc1278f72eb51fb9a3dc288944f.nq.gz
│   ├── 55b01c5354750d0b3b9184a611d46a48d1cfd2d6.nq.gz
│   ├── 566a45a213746a1276632f527845467c035e0793.nq.gz
│   ├── 591be5b0b8ae4559b3e4768fdd66032bd29b136c.nq.gz
│   ├── 5ee7812edbb236187b2434d8d01342f71c10b922.nq.gz
│   ├── 7547f6e1a919fe85b09e728cab15485f12cc9b1e.nq.gz
│   ├── 75f9a60a3189f805e8dd1691e620fc77856ff35b.nq.gz
│   ├── 84d4923409778711ac41820e6a5ccc25275e00ca.nq.gz
│   ├── 8dad3176921a4ca91cf4514c24f230ec223e22fa.nq.gz
│   ├── 8df41260800c3acd06ae29b21731d0db4a24128d.nq.gz
│   ├── 91c1918e7f727f022e2b0b095832b7483a0e2068.nq.gz
│   ├── 951f23b02fb7101c216de6290491899c68aba91c.nq.gz
│   ├── a440a9bd16b7b0926d6ad0e5a578bd64ee007e77.nq.gz
│   ├── b5f56f101ec4fc56852f0b4cc3120371b85c3bcc.nq.gz
│   ├── c5239eed7bf1c03b4acca7b6c59e5c662ac6cd5c.nq.gz
│   ├── c774563577e802c2cc230fb0ccc9ab1f3720b41e.nq.gz
│   ├── cb0e078e104d7292e8e80be265ee0c380ab0c740.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ea5b60640b01f74e295037aa8a6b7d4ea278a739.nq.gz
│   ├── f288702d2fa16d3cdf0035b15a9fcbc552cd88e7.nq.gz
│   ├── f71b322d2aabd560774185ebb7c3fec99c47ef3e.nq.gz
│   ├── fd37829deff94d3dc66b2a98cbf0a6171e8a4699.nq.gz
│   ├── ff95bb8217b6b64162a2911f958f8c367bebec4c.nq.gz
│   └── fff45eedf70d7a0a2879c732fecd310011350fb8.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── bad7f03f9c3ac3f98915a6c9751543264da03773.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 41 files
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

[ansible-community/antsibull-tool](https://github.com/ansible-community/antsibull-tool)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
