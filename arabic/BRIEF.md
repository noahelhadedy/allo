# Allo Arabic: design brief

Status: step 1 of 3 (brief). Nothing drawn or picked yet.

## Ground rules (read before any work)

- Allo Arabic is a new, original Arabic companion to Allo, released under OFL 1.1 with a NEW family name.
- The Thmanyah typeface is a mood reference only, seen as a reader. Its licence forbids modifying it,
  deriving from it, or redistributing it, and "thmanyah" is a reserved name.
- Never open Thmanyah font files in any tool, never trace, never copy outlines, metrics, spacing or kerning.
- Never name or market this as "like Thmanyah", a Thmanyah alternative, or anything Thmanyah related.
- Every Arabic outline comes from an OFL source (step 2) or is drawn from scratch here.
- Noah works at Thmanyah: check the employment contract (IP / conflict of interest) before any public release.

## What Allo is (the partner we match)

Allo is a warm, screen-first neo-grotesque based on Inter: "warm without being too cute, clear without being too cold".
Three axes: opsz 9-32 (default 14), wght 100-900 (default 400), ROND 0-100 (default 50).

Measured from the source (master opsz14 wght400 ROND50, 2048 UPM):

| Metric | Value |
|---|---|
| x-height | 1118 |
| Cap height | 1490 |
| Ascender / descender | 1984 / -494 |
| Win ascent / descent | 2061 / 494 |
| Stem (l), wght 100 / 400 / 580 / 900 | 45 / 178 / 258 / 398 |
| Advance n / o / H / space | 1188 / 1214 / 1495 / 554 |

## The Arabic we want (target feel, in words)

1. **Mood:** modern, calm, friendly, editorial. Feels at home in an app UI and in a long article.
   Confident, not loud. Same personality as Allo: warm but clear.
2. **Structure:** simplified Naskh skeleton with a light Kufi discipline. Horizontal, steady baseline,
   clear joins. No calligraphic flourish, no stacked ligatures beyond lam-alef.
3. **Contrast:** low, close to monolinear like Allo. Small optical thinning at joins only.
4. **Counters and bowls:** open and generous so ص ط ف ق ه و stay readable at 12-14 px.
5. **Terminals:** cut flat or slightly angled, then softened by the ROND axis
   (ROND 0 = crisp cuts, ROND 100 = round ends), matching Allo.
6. **Dots:** clear, slightly generous, shape follows ROND (square to round). Never fused to letters.
7. **Proportions:** medium width, not condensed. Teeth (سـ شـ) even and calm. Descending tails
   (ع ح ي ن ر) shorter than classical Naskh so line height stays close to Latin.
8. **Rhythm with Latin:** in a mixed line (Arabic + English UI labels, numbers) both scripts look
   like the same weight, size and colour. No script should jump out.

## Technical targets

- **Size match:** Arabic main body (tooth / bowl height) close to Allo's x-height (about 1050-1150).
  Alef close to cap height (about 1450-1550), never above the ascender.
- **Weight match:** Arabic stems about 90-95% of the Latin stem at the same wght
  (Arabic reads darker), e.g. about 165 at wght 400.
- **Vertical metrics:** Arabic descends deeper than Latin, so descender and win descent will grow
  (expect about -700 to -800). Lock final values before drawing so line height stays stable.
- **Axes:** cover wght 100-900 and ROND 0-100 from the start. opsz can follow later (spacing first, like Allo).
- **Character set (v1):** Arabic letters and all joining forms, lam-alef, hamza forms, harakat,
  Arabic and Persian/Urdu digits, Arabic punctuation (، ؛ ؟ ٪), tatweel, Persian/Urdu extras (پ چ ژ گ ک ی).
- **Features:** init / medi / fina / isol, rlig, calt, mark, mkmk, kern. Latin tnum style for Arabic digits.
- **Mixed UI:** test with real strings: buttons, prices with ر.س, dates, numbers, Arabic + English in one line.

## Next steps

2. Pick 3-4 OFL Arabic candidates against this brief, and show each beside Allo in a specimen.
3. Adjust the chosen one to Allo's metrics and axes, rename, build and test.
