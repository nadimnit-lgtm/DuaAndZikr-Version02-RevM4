# Dua & Zikr — Rev-L (Content Cleanup Pack applied)

Validator + logic tests + JS syntax pass. Total items: 181 (content_version 2.7.0-clean).

## What this is
Applied your uploaded "Azkar Content Cleanup Pack" (clean_content.py + manifest)
to the current content.json. Note: the pack assumed a 229-item input, but the
target IDs matched the maintained 185-item file (6/6 replacements, 2/2 renames,
6/8 removals present; the other 2 removals were already done in the earlier
audit), so it applied cleanly.

## Applied
- Removed 6 partial-duplicate fragments (Quran 2:286 pieces, Muslim 1342 travel
  fragments, a Qunut/ruqyah partial).
- Added 2 complete items:
  - "Pardon, Forgiveness, Mercy, and Victory" — full Quran 2:286.
  - "Complete Dua for Travel" — full Sahih Muslim 1342 (takbir + journey dua).
- Replaced 6 items with fuller wording (e.g. Wellbeing in this world & hereafter
  Abu Dawud 5074 / Ibn Majah 3871; Asking for all good Ibn Majah 3846; full wind
  dua Abu Dawud 5099; 71:28 parents; 3:193 caller; 43:13-14 mounting).
- Renamed 2 true excerpts with an "Excerpt:" prefix and is_excerpt flag
  (20:25-26 Musa; 26:83-85 Ibrahim).
- Renumbered priorities; recalculated total_items; recomputed sections.json
  counts to match.

## Net effect
185 -> 181 items. Urdu coverage preserved (23 items). No exact-Arabic duplicates
were found to merge (the file was already clean on that front).

## Note vs my earlier decision
The pack consolidates Quran 2:286 into ONE complete ayah; my earlier audit had
kept three distinct sub-supplications of 2:286. The pack's approach (one complete
verse) now applies, per your instruction to incorporate it.

## Pending review (unchanged)
The pack itself states it is a data-cleaning pass only. New/changed content and
all Urdu remain pending qualified scholarly / Urdu-literate review.
