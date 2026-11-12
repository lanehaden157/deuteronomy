# Deuteronomy Study — Style Reference

Deuteronomy's differences from `fragment-contract.md` (shared, read first). This
file wins. ✎ marks what the book decides. A book may instead keep a full
contract here.

## Components ✎

Optional components on: echo, list (`book.json` `"components"`; markup in
`components-reference.md`). Note here where this book uses each, and which
handoff box kinds it has.

## Hebrew in English ✎

**Transliteration** follows core's Hebrew adapter (`biblecore/lang/hebrew.py`):
diacritic only where the plain letter is already claimed (`ḥ ṭ ś`, `ʾ`/`ʿ`);
no vowel length; no spirantization; dagesh forte doubles; divine name `YHWH`,
rendered **Yahweh**.

**Translation.** Fresh, wooden-but-readable rendering from the Hebrew, not a
polish of an existing English version. Creative, intentional glosses
encouraged.

**Ids.** One root often spans several Strong's numbers, and one number can
bundle senses worth splitting. Bare id (`2416`) claims every lexeme under the
number; suffixed id (`2416e`) claims exactly one.

## Judgment ✎

- Structure markers: Masoretic paragraph breaks (`candidate-boundaries.md`).
- Names are joined by hand: place-name wordplay is real, Strong's etymology
  unreliable.
- ✎ Genre cautions (lists, law, poetry, …): add as units surface them.

## Unit map ✎

From the project side as `deuteronomy-literary-unit-map.md`.
`python -m biblecore units-from-map` loads its **Overview** table; keep this
shape:

    | # | Passage | Working title |
    |---|---|---|
    | | **PART ONE — Label (1:1–25:18)** | |
    | | *I. Label (1:1–10:10)* | |
    | 01 | 1:1–54 | Title |
    | 17 | 16:36–17:13 [Heb 17:1–28] | Title |

Bold row opens an outer grouping, italic an inner one; both optional. Passages
in English numbering, Hebrew difference in `[Heb ...]`.
Renumbering after units ship means editing `threads.json` opens/payoffs, every
`retro` entry and every fragment's meta block: confirm the map before unit 1.
