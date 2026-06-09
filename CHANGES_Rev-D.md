# Dua & Zikr — Rev-D (content expansion, batch 2)

Validator + logic tests pass. **Total items: 182** (content_version 2.4.0).

## Count trail
189 (original) → 170 (Rev-A dedup) → 175 (Rev-B +5) → **182 (Rev-D +7)**.
Net new authentic-sourced items via approach C so far: **+12**.

## Added this batch (+7) — all with English + Urdu, references verified
Approach C: Arabic is public-domain source text, translations are the app's own,
references checked by search, every entry flagged `pending_scholarly_review`.

| Item | Section | Reference |
|---|---|---|
| Tashahhud (At-Tahiyyat) | In-prayer (Azkar) | Bukhari 6265; Muslim 402 |
| Turning Over During the Night | Before Sleep | Nasa'i (al-Kubra) 10700 |
| Seeking Refuge from a Bad Dream | Before Sleep | Abu Dawud 3893; Tirmidhi 3528 |
| Seeing the New Moon | Daily Life | Tirmidhi 3451; Darimi 1811 |
| When Fearing a People | Daily Life | Abu Dawud 1537 |
| After Drinking Milk | Daily Life | Abu Dawud 3730; Tirmidhi 3455 |
| Thanking One Who Does Good | Daily Life | Tirmidhi 2035 |

## Skipped (on purpose)
- **Before Sleep: Tasbih 33/33/34** — its Arabic is identical to the existing
  "After Salah: Completing One Hundred" entry, so the dedup guard skipped it
  rather than create a duplicate (the validator rejects duplicate Arabic). The
  text is already in the app; only the context differs.

## Urdu coverage now
19 items carry draft Urdu (12 from Rev-C + the 7 here), still
`urdu_status: draft_pending_review`. Remaining items show English until
translated. Next Urdu batch suggestion: Morning, Evening, Kalimas.

## Still pending review (unchanged)
All new content and all Urdu translations require scholarly / Urdu-literate
sign-off before being treated as final. Build once through CI before publishing.
