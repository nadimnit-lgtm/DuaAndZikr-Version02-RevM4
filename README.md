# Azkar TV Display — Version 02

A calm, offline Islamic reading app for Android **phones, tablets and Android TV /
Google TV**. It presents one authentic Dua, Dhikr (Azkar), or Kalima at a time with
the Arabic text as the reading focus, accompanied by transliteration, a natural
English translation, and a sourced reference.

## What's new in Version 02

- **Three content categories** — Azkar, Dua and Kalima — with the six Kalimas kept
  as their own set.
- **Mixed Flow** (default): cycles Azkar → Dua → Kalima → repeat, for manual
  navigation and auto-rotation alike. A "Single category" mode and fine-grained
  "Browse by section" are also available from the picker.
- **Indo-Pak Arabic script** (Noto Nastaliq Urdu) applied by default, with a
  high-clarity **Naskh** (Scheherazade New) option for maximum legibility.
- **Dynamic text fit**: Arabic shrinks to fit the card so it never clips, compresses,
  or breaks one word per line; long content scrolls vertically and never spills
  outside the card.
- **Easy View** for larger Arabic, buttons and spacing.
- **Android TV / Leanback** support: home-screen banner, D-pad navigation
  (left/right move items, up/down scroll, OK pauses/resumes auto-rotation, Back
  closes an open panel first), and large sofa-distance focus rings.
- Large labelled Previous / Next buttons, regrouped settings
  (Display / Content / Navigation / Prayer / About), a high-contrast quick toggle,
  and a subtle Islamic-geometry backdrop.
- Optional **Copy** control on each card (hidden on TV).

## Highlights

- One-item reading view with the Arabic text as the hero element.
- Responsive layouts for phone portrait, phone landscape, tablet portrait, a
  two-zone tablet landscape layout, and a dedicated TV layout.
- Swipe left or right to move between items; vertical scroll for long text;
  long-press the card (or press OK on TV) to toggle auto-rotation.
- Five themes: Dark Ambient, Gold and Navy, Haram-Inspired Light, Green Classic,
  and High Contrast.
- Compact, optional prayer-time ribbon (Umm al-Qura, method 4) with manual city
  selection. Offline values are clearly labelled as approximate.
- Content served to the WebView through a secure asset loader on an HTTPS origin.
  Cleartext traffic and file-URL access are disabled.

## Build

The project builds with Gradle and the Android Gradle Plugin. The included GitHub
Actions workflow validates content, runs logic tests, and produces a debug APK on
every push.

- Application ID: `com.ahmed.azkartv`
- Version name: `Version 02`
- Version code: `2`
- minSdk 22, targetSdk 34, compileSdk 34, JDK 17
- The same APK installs on phones, tablets and Android TV (Leanback is declared
  optional and touchscreen is not required).

## Tests

- `python3 tools/validate.py` — content validation: duplicate IDs / Arabic / titles,
  required fields, verification flags, repeat values, `main_category` and
  `size_mode` enums.
- `python3 tools/test_logic.py` — logic contracts: repeat parsing, mixed-flow
  ordering, settings round-trip, category bucketing, and app.js wiring.

## Content note

All items carry a source reference and a verification flag. The content set is
prepared with care but has **not yet been confirmed by a qualified scholar**. The
top-level `review_status` is `pending_scholarly_review`. Tajweed colouring is only
enabled where verified Quranic markup is bundled; none is included in this version,
so it stays off.

## Fonts and licences

- **Noto Nastaliq Urdu** (Indo-Pak Arabic) — SIL Open Font License 1.1.
- **Scheherazade New** (Naskh Arabic) — SIL Open Font License 1.1.
- **Amiri**, **Reem Kufi** — SIL Open Font License 1.1.
