# Deuteronomy Study — Style Reference

Deuteronomy's differences from `fragment-contract.md` (shared, read first). This
file wins. ✎ marks what the book decides. A book may instead keep a full
contract here.

## Components ✎

On: echo, list, digest, story, synoptic, mirror, lawparallel (`book.json`
`"components"`; markup in `components-reference.md`).

- **echo:** Moses quoting or recasting earlier Torah; NT quotations (Matt 4, 22).
- **list:** blessing and curse catalogues, the Ten Words, lists of prohibited things.
- **digest:** units and stretches marked condensed or digest in the unit map.
- **story:** an earlier event the speech points back to without retelling it
  (Miriam 24:9, Amalek 25:17–19, Baal Peor 4:3, Sodom and Gomorrah 29:23,
  Dathan and Abiram 11:6).
- **Side by side** (the synoptic box under that label): Moses' retelling of an
  event Exodus–Numbers narrates (Horeb, Kadesh, the calf).
- **mirror:** the Leviticus twin, only for a pair the unit pack's mirror section gives.
- **lawparallel:** a law restated elsewhere in the Torah (`laws.json`).

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
- ✎ Genre cautions (**TENTATIVE draft**; more as units surface them):
  - Speech: Moses speaks; mark when a line is Yahweh quoted, Moses' own, or narrator.
  - Law: state each statute's own reason clause; compare Exodus/Leviticus parallels for differences only.
  - Poetry (chs. 32–33): lines as the Hebrew parallelism falls; difficult text flagged, not smoothed.
  - Curses: conditional, rhetorical; present as written.
  - Numeruswechsel: keep singular/plural "you" visible per `translation-choices.md`.
  - Verse numbers: English in prose and refs, `[Heb ...]` only where the corpus is addressed.

## Unit map ✎

From the project side as `deuteronomy-literary-unit-map.md`.
`python -m biblecore units-from-map` loads its **Overview** table; keep this
shape:

    | # | Passage | Working title | Tier | Peak |
    |---|---|---|---|---|
    | | **SPEECH — Label (1:1–4:40)** | | | |
    | | *I. Label (4:41–11:32)* | | | |
    | 01 | 1:1–18 | Title | condensed | |
    | 07 | 5:1–33 | Title | full | ★ |
    | 24 | 22:1–30 [Heb 22:1–23:1] | Title | condensed; 22:5–12 full | |

Tier: full, condensed or digest, plus `; <verses> <tier>` stretches. A peak is full.

Bold row opens an outer grouping, italic an inner one; both optional. Passages
in English numbering, Hebrew difference in `[Heb ...]`.
Renumbering after units ship means editing `threads.json` opens/payoffs, every
`retro` entry and every fragment's meta block: confirm the map before unit 1.
