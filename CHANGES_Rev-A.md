# Azkar TV Display — Content Correction Pass (Rev 02-A)

Basis: data-integrity & classification audit of `content.json`.
Scope: structure, classification, de-duplication, titles, repeat model, and
verification governance. **Content authenticity is NOT certified here** — it
remains pending qualified scholarly review (see Open Items).

Result: **189 → 170 items**, validator passes, build vocabulary kept in sync
across `content.json`, `sections.json`, `app.js`, `app.css`, `tools/validate.py`.

## Closed findings

| # | Severity | Finding | Action taken |
|---|----------|---------|--------------|
| C1 | Critical | 125 items flagged `verification:"authentic"` while the header says nothing is verified | Removed the authenticity claim entirely. `verification` now denotes **provenance only**: `quran` / `hadith` / `compilation`. Global "provisional until reviewed" disclaimer retained. |
| C2 | Critical | Same hadith reference carried different flags (Muslim 2723, 591, 771) | Flag is now derived deterministically from the source string — identical source always yields the identical flag. Conflicting-flag count: **0**. |
| H1 | High | After-*adhan* dua (Bukhari 614) filed under *After-Salah* Azkar | Moved to a new dedicated **After Adhan** section; re-typed as Dua; retitled "Supplication After the Adhan". |
| D1 | High | Dua al-Qunut triplicated (1 fragment + 2 identical full texts) | Kept one complete Qunut (with the fullest source citation); removed the fragment and the duplicate. |
| D2 | High | Concatenated/fragment after-salah entries triple-counted content | Removed the concatenation ("Seek S Forgiveness Three") and the lone "Alhamdulillah" fragment; kept the atomic adhkar. |
| D3 | High | Same dhikr under inconsistent romanization (Sayyid/Sayyidul) | Kept the single complete "Sayyid al-Istighfar"; removed the **truncated** morning copy (it contained only half the dua). |
| Q1 | High | Machine-mangled titles shipping to users | 15 titles rewritten by hand (e.g. "Name O Die Live" → "Before Sleep: In Your Name I Die and Live"; "O Submit Myself Entrust" → "Before Sleep: I Submit Myself to You"; "Seek S…" removed). |
| Q2 | High | `repeat` semantics incoherent on compound dhikr | Compound tasbih entries set to `repeat:null` (per-phrase counts live in the text); two attested completion methods kept and clearly titled. |

### De-duplication detail (19 removed)
Most "duplicates" were **truncated fragments** of a fuller supplication — a
quality defect in itself (a Qur'anic dua cut short). Kept the complete version,
removed the fragment, in: 2:128, 3:8, 10:85-86, 26:83-85 (3 fragments), 27:19
(2 fragments), 71:28, 59:10, Muslim 2723 morning & evening "dominion", and the
dua-for-pain variant. Distinct sub-duas of the same verse (e.g. the three
separate supplications within 2:286) were **kept**.

## Open items (require a qualified scholar — not done here)
1. **Authenticity grading.** Provenance flags are not a ruling on ṣiḥḥah.
   Each `hadith`-flagged entry still needs grading confirmation.
2. **After-salah tasbīḥ count.** Two attested forms retained (33/33/34 and
   33/33/33-completing-100). Reviewer to confirm/consolidate.
3. **Dua-for-pain wording.** Variants differ ("billāhi" vs "bi-ʿizzatillāhi",
   Bismillāh ×3 prefix). Reviewer to reconcile to one attested wording.
4. **Retained cross-context overlaps (7).** Same dhikr in two valid contexts
   (e.g. Āyat al-Kursī before-sleep vs protection) or a short phrase embedded
   in a longer compound — kept by design; reviewer to confirm.
5. **Tajwīd (M1).** `tajweed_html` is null on all items and the feature is off.
   Not changed; product decision to populate or de-brand.

## Reference used
Structural/classification corroboration only (no text imported, copyrighted):
*Collection of Authentic Invocations*, compiled from Shaykh al-Albānī
(Authentic Statements Publishing). Its table of contents independently
separates "Remembrance Upon Hearing the Adhān" from "Remembrance Said After
the Prayer", corroborating finding H1.
