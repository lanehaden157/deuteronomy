# Improvements Log

Only what git can't show: a decision and why, something tried and reverted, a gotcha. Most recent last.

- Bootstrapped with `tools/new_book.py` from bible-core 0.31.0 (`7f91ee5`): template, vendored core, lexicon, npm + corpus. Check the corpus counts against a printed edition.
- Mirror seed pairs have no chiasm tier on purpose: Tigay's Deut 28 chiasms are internal to the chapter, and no Lev 26 order is claimed. All pairs are tier echo; Lane decides strength and any pos.

- 2026-11-13: book.json groupings are `["speech","treaty","part"]` (speech first: it drives the map and covers all 36 units; `part` covers only 5:1–29:1). Always run `units-from-map --kinds speech,part`: the default (book.json reversed) would take `treaty` as a kind. The treaty entries live only in data/units.json; units-from-map is additive and a rerun kept all 9 (checked). Treaty "detailed stipulations" lists units 7–28 with verses only where the unit is partly in it.
- 2026-11-13 (core 0.37): `story` enabled for Deuteronomy (events the speech points back to without retelling: Miriam, Amalek, Baal Peor); retellings of Exodus–Numbers events stay Side by side (synoptic). `resources.md` names research files flat (`figures-tigay.md`); the sync mirrors flat. `python -m biblecore sync` commits AND pushes.
