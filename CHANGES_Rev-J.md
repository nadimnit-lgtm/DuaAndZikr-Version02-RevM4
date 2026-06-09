# Dua & Zikr — Rev-J

Validator + logic tests + JS syntax pass. 185 items.

## 1. Indo-Pak / Nastaliq retired for Arabic (Naskh only)
- Removed the "Arabic script" toggle. Arabic now always renders in Naskh
  (Scheherazade New). Default changed to naskh; any saved "indopak" preference
  is auto-migrated to naskh on launch. CI test updated.
- Noto Nastaliq Urdu is kept ONLY for the Urdu translation text.

## 2. Recitation audio (auto + manual) — feature built; audio files are yours to add
- New "Recitation" setting: Off / Manual / Auto.
  - Manual: a play/pause button appears on each item.
  - Auto: plays on open and auto-advances to the next item when finished.
- Per-item audio resolves from an item's optional `audio` field, or from a
  configurable "Audio source" base URL (files named <id>.mp3).
- WebView updated to allow autoplay (mediaPlaybackRequiresUserGesture=false).
- IMPORTANT: no audio is bundled. I cannot supply Sheikh al-Sudais's voice
  (copyrighted recordings of a living person; I won't synthesize a real voice;
  a per-dua set in his voice does not exist publicly). Point "Audio source" at
  recitation files you have the right to use, or add an `audio` URL per item,
  and playback works immediately. Button stays hidden when no audio is set.

## 3. Simple mode cutoff fixed
- Root cause: the reader used flex `justify-content:center`, which clips the
  TOP of content that overflows — so enlarged Simple-mode text was cut off at
  the start and unreachable. Now uses `safe center` for normal sizes and
  top-aligns (flex-start) in Simple mode, so the beginning is always visible
  and scrollable.

## 4. Manual city list removed
- Location is live (GPS / network), so the Riyadh/Jeddah/Makkah/... presets are
  gone. Settings now shows a short "Automatic — based on your live location"
  note. Any saved manual city is migrated to automatic on launch.

## Pending review (unchanged)
New content and all Urdu remain pending scholarly / Urdu-literate sign-off.
