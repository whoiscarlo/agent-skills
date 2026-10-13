---
name: reverse-engineering-formats
description: Use when decoding or rebuilding an undocumented or partly documented file format, codec, compression scheme, or obfuscated field; when reimplementing a closed app's output with no reference implementation to diff against; or when tests for a decoder or renderer need ground truth.
---

# Reverse Engineering Formats

## Overview

You cannot trust a decoder you cannot check. Before guessing at a format, find
an **answer key**: output the original software already produced, which your
code must reproduce. Then pin every finding as a test with a written margin.

Taken from the ArtCraft apps (Rust rebuilds of Photoshop, Lightroom, Premiere,
After Effects, Acrobat, Illustrator). Notes: `~/code/APPS/vault/ArtCraft/`.

## Answer keys, strongest first

| Answer key | Example | How to use it |
|---|---|---|
| Render saved inside the file | PSD merged composite; camera JPEG inside a raw | Render the layers, compare to it |
| Same content saved two ways | Same scene shot compressed and uncompressed | The plain copy is the truth for the packed one |
| Outside program run as a black box | ffmpeg, qpdf, DNGLab, rawpy | Run the binary, diff outputs. Never read its source, never link it |
| Original app driven by its own script API | After Effects `.jsx` sampling keyframes | Record numbers, fit formulas, commit the numbers as tests. Check the vendor's terms first |
| Weak key | Embedded thumbnail, stale preview | Fallback only. Calibrate its margin on files that pass a strong key. A fail here may be the key's fault |

## Techniques when the spec runs out

- **Search, then score with self-consistency.** For hidden tables (Nikon NEF
  Huffman), search candidate tables and keep the one where the whole stream
  decodes, ends within the last byte, and every value stays in range.
- **XOR known plaintext.** Two files whose plain values you know, XOR'd
  together, locate a hidden field (Sony ARW black level at byte 2510).
- **Fit the transform from output alone.** Sony ARW bytes turned out to be
  `p^3 mod 249`; try simple algebra on input and output pairs before anything
  clever.
- **Verify on breadth.** One camera proves nothing. Re-check on many devices
  from public CC0 samples (raw.pixls.us), about 45 files from 35 bodies.
- **Unknown means unsupported.** A variant you have not recovered returns an
  `Unsupported` error and falls back (to the preview, for example). Never guess.
- **Pull spec tables by script.** Extract tables from the standard's PDF with
  `pdftotext` plus a parser, so nothing is hand-typed or copied from another
  decoder.

## Pinning it as tests

1. **Write the margin and the reason.** Bit for bit for H.264; within 1 level
   for ProRes "different integer IDCT"; 2/255 for PSD composites.
2. **Floors that only rise.** Commit pass counts as constants
   (`pass_floor: 146`). CI fails if a count drops. Raise the floor when it
   improves.
3. **Missing judge fails CI.** Tests may skip locally without ffmpeg, but an
   env flag (`REQUIRE_ORACLES=1`) turns every skip into a failure in CI.
4. **Write down where the judge is wrong.** If ffmpeg disagrees with a
   hand-worked answer, record it next to the test.
5. **Record provenance in the module header.** List every source used and how
   each finding was derived, so the next reader can re-check it.

## Common mistakes

| Mistake | Fix |
|---|---|
| Testing only against your own encoder | Round trips prove consistency, not correctness. Add an outside answer key |
| One global tolerance | Set the margin per format, with its reason |
| Oracle tests silently skip in CI | Make missing tools fail under a CI flag |
| Refusing to compare against open-source decoders at all | Running the binary is fine; reading its source is what taints you |
| Committing vendor sample files | Rebuild what you learned as synthetic test files |

**REQUIRED SUB-SKILL:** load clean-room-agents before reading any outside
source, to know which sources are allowed.
