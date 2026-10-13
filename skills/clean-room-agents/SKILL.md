---
name: clean-room-agents
description: Use when AI agents will rebuild, clone, or match the behaviour, file formats, or look of a closed commercial app or another project's code, or when writing AGENTS.md or CLAUDE.md rules about what sources agents may read.
---

# Clean-Room Agents

## Overview

A clean room means your code is written only from allowed knowledge
(specs, observed output), never from the original's code or assets. With
agents, the rules must live where agents read them (`AGENTS.md`) **and** be
enforced by checks, because agents are very good at finding things on disk.

This is engineering practice, not legal advice. Read the vendor's terms.

## The rule set (copy and adapt)

**Sources allowed**
- Public specs and standards, cited by URL in the code.
- Files users own, used locally, never committed.
- Outside programs (ffmpeg, qpdf) run as separate processes to judge output.

**Never**
- Read, disassemble, or list the contents of the vendor's app bundle,
  plug-ins, presets, profiles, help files or fonts.
- Read the **source** of other implementations, even permissive ones (dcraw,
  LibRaw, libvpx). Running their binary is allowed; reading their code is not.
- Copy vendor assets, even ones the vendor released under an open licence
  (Source Han fonts are banned in ArtCraft for this reason).
- Commit screenshots or notes of the vendor app. They live in a gitignored
  `plan/<app>/` folder.

**When unsure:** "If a task seems to need any of this, stop and say so."

## Decide on black-box observation explicitly

Running the vendor app to watch it is the grey zone. ArtCraft repos split:
EffectCraft scripts After Effects, while VectorCraft banned it after reading
that Adobe's terms forbid "observing a program's inputs and outputs to
recreate it". Read the terms, then write the decision into `AGENTS.md`.

## Enforcement beyond the rules file

| Check | What it catches |
|---|---|
| Asset manifest (one entry per file: source, licence, SHA-256) checked in CI | Unlicensed or vendor files |
| Build check failing on vendor file types and vendor-sounding names | Copied presets, profiles, icons |
| Closed allow-list of vendor data, changes need human approval | Slow creep of "just this one table" |
| Provenance header in each format module listing sources used | Lets a reviewer audit where knowledge came from |
| Test files pinned by commit and SHA-256 in a separate repo | Large or tainted binaries in the main repo |
| Sandbox or hooks hiding the vendor install from agents | Agents stumbling into the bundle |

**Verify every promised check exists.** VectorCraft's `AGENTS.md` says
`cargo xtask cleanroom` runs in CI; the command does not exist. A rule that
names a check nobody wrote is worse than no rule. Grep for it.

## Common mistakes

| Mistake | Fix |
|---|---|
| "Compatible licence, so we can read it" | Licence covers copying. Reading source still taints a clean room |
| Observation notes committed in `docs/` | Gitignored `plan/`; commit only the spec you derived |
| Rules only in prose | Back each rule with a CI check or a hook |
| Never deciding the black-box question | Decide once, in writing, after reading the terms |

RELATED: reverse-engineering-formats, parity-ledger.
