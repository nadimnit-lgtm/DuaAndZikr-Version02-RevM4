# Dua & Zikr — Rev-B (rename, global location, UI uplift, content batch)

Builds on Rev-A (content audit corrections). Validator passes: **175 items, 13 sections**.

## 1. Rename → "Dua and Zikr"
- `strings.xml` `app_name`, launcher label, `<title>`, splash name, and the
  `content.json` `app` field all updated.
- **Package id stays `com.ahmed.azkartv`** — changing it would break your
  existing signing/release pipeline and isn't needed for the display name.

## 2. Global, location-aware prayer times (was Saudi-only)
- `Location` setting now defaults to **Automatic**. Resolution order:
  **GPS/fused → network/IP (ipapi.co, ipwho.is fallback) → last-known cache → Riyadh approx.**
  This works worldwide, including on TVs with no GPS (they use IP).
- Prayer times fetched from Aladhan **by latitude/longitude**, with the
  calculation method chosen per country (`methodForCountry`, e.g. SA→Umm al-Qura,
  Gulf→Dubai/Qatar/Kuwait, US/Canada→ISNA, default→MWL).
- Manual Saudi-city presets retained as a fallback.
- Native plumbing: `ACCESS_COARSE_LOCATION` permission, `setGeolocationEnabled`,
  a `WebChromeClient` that grants geolocation to the trusted asset origin only,
  and a one-time runtime permission prompt. Denial is safe (IP fallback).

## 3. UI uplift (graphics)
Additive, theme-token-driven, no layout changes:
- Layered atmospheric background (top glow + corner light + vignette).
- Edge-faded geometry backdrop so it reads as texture.
- Reading card: depth, luminous gold hairline, subtle surface gradient, a calm
  rise-in entrance.
- Prayer ribbon: gradient + accent edge + glowing next-prayer label.
- Stronger D-pad/TV focus ring; brand-mark halo; `prefers-reduced-motion` honored.
- Graceful fallback where `color-mix` is unsupported.

*Visual taste is iterative — view it on the Panasonic and tell me what to push
or pull back.*

## 4. Content expansion — Approach C (first batch: +5)
Source: the al-Albani compilation was used **only as a topic checklist**. No text
was copied from it. Arabic is public-domain source text; **translations are the
app's own**; references verified by search; all flagged for scholarly review.

Added: Opening Supplication of the Prayer (Istiftah); Remembrance After Wudu;
Expiation of the Gathering (Kaffarat al-Majlis); Breaking the Fast; Supplication
for the Host.

### Suggested next batches (gaps vs the checklist — say the word)
- **In-prayer:** seeking refuge before recitation; between the two prostrations
  (have a variant); tashahhud; salawat in tashahhud.
- **Sleep cycle:** turning over at night; when startled; the Qul + Ayat al-Kursi
  bundle cross-linked to before-sleep.
- **Situational:** seeing the new moon; entering a town/lodging on travel; when
  fearing a people/enemy; debt relief (have one); difficulty made easy.
- **Qunut for calamity** (nazilah) in the five daily prayers.
- **Cross-link** Ayat al-Kursi + the three Quls into "After Salah" (they exist in
  Protection; an after-salah reference would complete that section).

All future entries follow the same rule: own translations, verified refs,
`review_status: pending_scholarly_review`.
