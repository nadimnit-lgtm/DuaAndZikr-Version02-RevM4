# Dua & Zikr — Rev-M (full Salah cycle: Before / Inside / After)

Validator + logic tests + JS syntax pass. Total items: 206 (content_version 2.8.0).

## Architectural change
Validator duplicate-Arabic check is now PER-SECTION, not global. The same dhikr
may legitimately appear in different occasions (e.g. Ayat al-Kursi and the three
Quls appear both in protection and after salah), as in standard adhkar books.

## New structure (from your curated Salah table)
Three coherent sections now drive the browse list and search:

### Before Salah (6)
Before Wudu (Bismillah), After Wudu (shahada + tawwabin), Entering the Masjid,
Entering the Masjid with Salawat, Salawat After the Adhan, Dua After the Adhan.

### Inside Salah (25)
Takbir al-Ihram; three opening supplications + the night-prayer opening; seeking
refuge; Basmalah; ruku tasbih + Subhanaka + Subbuhun Quddusun; Sami Allahu;
Rabbana wa lakal-hamd + extended praise; sujud tasbih + three sujud duas; both
between-sujud forms; Tashahhud; Salat Ibrahimiyyah; Protection from Four Trials;
Dua of Abu Bakr; Witr Qunut; Taslim.

### After Salah (14)
Istighfar; Allahumma Antas-Salam; Tahlil; Allahumma la Mani'a; La Hawla form;
Tasbih 33/33/34 + Completing One Hundred; Ayat al-Kursi; al-Ikhlas; al-Falaq;
an-Nas; Help to Remember/Thank/Worship; After-Fajr beneficial knowledge.

## How it was done
- Moved 13 existing items (istiftah, tashahhud, ruku/sujud/rising dhikr, Darood,
  Qunut, Four Trials, after-wudu, entering masjid, after-adhan, Help-to-Remember)
  into the right Salah sections, PRESERVING their Urdu.
- Added 25 new items with own English translations + verified references, flagged
  pending review.
- Net 181 -> 206.

## Deliberately NOT added (with reason)
- Replying to the adhan, dua between adhan & iqamah, "no fixed niyyah formula",
  Qur'an after al-Fatihah, "general dua in sujud" -> these are instructions, not
  fixed-wording duas, so they don't fit a dua card.
- Al-Fatihah as a whole surah -> not stored as a dua entry.
- Tasbih 10/10/10 -> identical Arabic to the 33/34 tasbih already in After Salah
  (differs only in count), so it was folded in rather than duplicated.

## Pending review (unchanged)
New content and all Urdu remain pending qualified scholarly / Urdu-literate review.
