# Repolex Knowledge Graph of piccolo-orm/targ

RDF knowledge graph data for [piccolo-orm/targ](https://github.com/piccolo-orm/targ), parsed by [repolex](https://repolex.ai).

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
rlex download piccolo-orm/targ
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 40c882080289080fbdad2dc8b87e71f7a31d2657
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 40c882080289080fbdad2dc8b87e71f7a31d2657
│           └── chunk-001.nq.gz
├── blob
│   ├── 040ebd2813d1e9d5b174cbdcc284e3b07abea1cb.nq.gz
│   ├── 066b91b4df0c13f5adca7a4e5c20d743b9574aa5.nq.gz
│   ├── 09ca3b6290a7ce279f77163aa02a2a02499ef1d8.nq.gz
│   ├── 298c25c3d2390e7f00345daf16bb7439a1e62ef0.nq.gz
│   ├── 30e0cef58a147bde42d5bd9aeeafc3ed42c7591b.nq.gz
│   ├── 40a65a286b0cf4d8d929cc15d46523bc3cc40056.nq.gz
│   ├── 5c868eb1a25382f11ec22304e7a549ef0dd504ee.nq.gz
│   ├── 6450d9930f0b4af036c891579d00119c15d76416.nq.gz
│   ├── 64e9c55446a4d3623cfd9df0e2a8d0c07fcd6000.nq.gz
│   ├── 6b3b7f9d7581b26de9f149820a4918a610ef66c7.nq.gz
│   ├── 76b585b359122796c86b9ed3eb150285292f156d.nq.gz
│   ├── 80fcc80fe6fbad4b9e1074e253ceeceae04695e7.nq.gz
│   ├── 8db118e9bc9cc9129c777594bb7aa8d92179a512.nq.gz
│   ├── 8e47adc1927567e9e6449c744b73f7f4613b7bcb.nq.gz
│   ├── a72b6b8d4198ab6f60391a883b1a6af8a709360f.nq.gz
│   ├── a8251307451dd9e29aed1a477778d3d15a0030ae.nq.gz
│   ├── ace7ceaa661ab95c5c3b34ddf12db29cc8941a37.nq.gz
│   ├── aeb06748ff717989f478e054d5a11f68285470c2.nq.gz
│   ├── b063722a93d8338c02b75ba14b17db79d90b8762.nq.gz
│   ├── b1fce66f6c57f65b8139a800a871b34ac92b49d1.nq.gz
│   ├── b50109c0bc6ead430eeeee9021bf243e073a376b.nq.gz
│   ├── c2f64d1b021bed5802d7215eaa846955c31c0c1a.nq.gz
│   ├── c5bdf5bf5c798c3a94b20cd000ad588ee39606a0.nq.gz
│   ├── c72bf4ba6d3d654e9427b313c92a0c95c23aa7b1.nq.gz
│   ├── c7c069650413524628df0bc1394c28949d6e5fd8.nq.gz
│   ├── c9cb68356430c68217ae687d4d1ca58bd5bf3164.nq.gz
│   ├── cafdfe1517ac9884b7abbf6ebdad328bfbc1dda3.nq.gz
│   ├── d3c982b6d7fa7e8bac6090ffabddc804ba285180.nq.gz
│   ├── d76c92b6f8ccc72630aac7f77c44dd1c86a64a82.nq.gz
│   ├── d84cc51b8629f633aaf6b38791ef418e6f1d52f8.nq.gz
│   ├── d8bd1ec2b386cff7bd2b5e28bc94a6390594f6a1.nq.gz
│   ├── df12fa757e04987c1c158c00e0584675d161b3e1.nq.gz
│   ├── e62e528d62af2be641d2834f475b1107060059f6.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── efc620bb2cf46b127a9efcb82f48a2c20cedb89b.nq.gz
│   ├── f245cd13a06e4b35532667f49b2855f7a80c0075.nq.gz
│   ├── fb2159b2fa505dc2552776ff7529d9cf5430c2e9.nq.gz
│   ├── fbff3ac21916fa8c035c5e00f824b41a5087383f.nq.gz
│   ├── fd902666db220612a0794bb6849a3333f8192721.nq.gz
│   └── ff4f565bb7dd60e4c999752a6ab14776b599d939.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 40c882080289080fbdad2dc8b87e71f7a31d2657.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 48 files
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

[piccolo-orm/targ](https://github.com/piccolo-orm/targ)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
