<p align="center">
  <img src="https://raw.githubusercontent.com/holt-os/holt/main/docs/header.png" alt="Holt" width="100%">
</p>

<p align="center">
  <a href="https://github.com/holt-os/holt"><img src="https://img.shields.io/badge/repo-holt--os%2Fholt-181717?logo=github" alt="holt-os/holt"></a>
  <a href="https://www.npmjs.com/package/@holt-os/holt"><img src="https://img.shields.io/npm/v/@holt-os/holt?logo=npm&color=cb3837&label=npm" alt="npm version"></a>
  <a href="https://productsdecoded.com/holt"><img src="https://img.shields.io/badge/docs-productsdecoded.com%2Fholt-f5a623" alt="Docs"></a>
  <img src="https://img.shields.io/badge/license-MIT-blue" alt="MIT license">
</p>

***

**Holt is an open-source personal agent OS.** It runs in a folder on your own machine, uses whichever LLM you point it at, and keeps a memory of your work as plain files you can read and edit.

> A *holt* is a small wood: a sheltered place where things are kept and grow.

## Install

Homebrew pulls Node in for you:

```bash
brew install holt-os/tap/holt
```

Or with npm, if you already have Node 20 or newer:

```bash
npm i -g @holt-os/holt
```

Then `cd` into a folder you want to work in and run `holt`.

## What lives here

| Repo | Why it exists |
|---|---|
| **[holt](https://github.com/holt-os/holt)** | The CLI itself: brains, memory, the ten bundled skills, the knowledge graph, the wiki, the MCP server. Start here. |
| **[homebrew-tap](https://github.com/holt-os/homebrew-tap)** | The formula behind `brew install holt-os/tap/holt`. Nothing else to see. |
| **[registry](https://github.com/holt-os/registry)** | Community skills that do not ship in the box, plus the `registry.json` index that `holt skill search` reads. |
| **[holt-jobsearch](https://github.com/holt-os/holt-jobsearch)** | A job-search agent built on Holt: profile, fit score, tailored resume, cover letter, tracker. It drafts, you hit send. |
| **[holt-benchmarks](https://github.com/holt-os/holt-benchmarks)** | Holt's scores on LongMemEval, LoCoMo and BEAM, with every answer, grade and the code to rerun them. |

Running agents across a team? **[Holt Teams](https://productsdecoded.com/holt/teams)** is governed, self-hosted shared memory built on the same engine. It is a separate product, not in this org, and I'm taking design partners.

## Memory you can open

Every exchange lands in `.holt/memory/turns.jsonl` inside the folder you launched from. Holt distills durable facts from a session into a `facts.md` you can read and correct by hand, and `holt wiki` folds those facts into cross-linked Markdown that Obsidian opens as a vault. `holt graph` writes one self-contained HTML file, no server and no CDN, showing how it all connects.

Recall matches by meaning once you enable the local Ollama embedding model, and falls back to word overlap if you skip it. Memory is per folder and isolated by default; `holt memory global on` opts a folder into a shared store when you want knowledge to cross over.

## Memory you can check

| Benchmark | Holt 0.19 |
|---|---|
| LongMemEval (graded by GPT-4o) | **91.2%** |
| LoCoMo | **88.2%** |
| BEAM, 1M tokens | **79.6%** |

Every question, answer and grade is public in [holt-benchmarks](https://github.com/holt-os/holt-benchmarks), so you can check the numbers instead of trusting them.

## Docs

Install steps for macOS, Linux and Windows, the full command reference, and a setup guide written for people who have never opened a terminal: **[productsdecoded.com/holt](https://productsdecoded.com/holt)**

Going deeper, in the main repo: [ARCHITECTURE.md](https://github.com/holt-os/holt/blob/main/ARCHITECTURE.md), [CONFIGURATION.md](https://github.com/holt-os/holt/blob/main/CONFIGURATION.md), [CONTRIBUTING.md](https://github.com/holt-os/holt/blob/main/CONTRIBUTING.md).

MIT licensed. The command surface is still moving between releases, so where a cached page and the docs site disagree, I would trust the docs site.
