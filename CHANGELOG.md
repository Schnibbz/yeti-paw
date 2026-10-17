# YETI PAW — Changelog

Two numbered tracks, so a document update never bumps the hardware number:

- **Hardware** (`v1.x`): the printable parts, the parts list, print settings and safety factors. Tags `v1.2`, `v1.3`, …
- **Research** (`research-v1.x`, `research-v2.x`): the handle-design study PDFs. Tags `research-v1.0`, `research-v2.0`, …

Every version is a tagged [GitHub Release](https://github.com/Schnibbz/yeti-paw/releases) with its own files attached, so
older versions stay downloadable. The files in the repo itself are always the latest.

## Hardware v1.3 — 2026-10-17

> ### ⚠️ Two parts changed. Buy the new ones.
>
> | Part | v1.2 (old) | **v1.3 (new)** |
> |---|---|---|
> | **Handle bearing** · 2 per handle · both plate variants | FR8-2RS **flanged**, 1/2" × 1-1/8" × 5/16" | **R8-2RS plain** (no flange), same size |
> | **Carabiner eye sleeve** · 1 per yoke | uxcell **wrapped** flanged sleeve, 20 × 23 × 10 mm, Ø30 flange | **Solid bronze plain sleeve**, McMaster **6391K256** (3/4" bore × 7/8" OD × 1/2" long) |
>
> They don't interchange: v1.3 plates have no flange pocket, and the v1.3 eye bore is Ø22.29 for the 0.877" bronze sleeve.

- **Side plates (both variants):** handle seat for the plain R8: a straight Ø28.62 seat from the outer face to the Ø21
  ledge; the flange pocket and the support it needed are gone. Print settings updated (two support areas instead of three).
- **Carabiner yoke:** eye bore Ø22.29 = the sleeve's specified OD (0.877" +0.001/−0), the same zero-allowance press rule
  the handle seat was fit-tested on. The sleeve (0.500" ± 0.005") sits flush with both faces of the 1/2" eye, so the
  carabiner bears only on bronze. Why: the wrapped sleeve pressed in out of round and left the bottom rim bare plastic.
- **Centered-pivot plates:** the yoke-to-handle side is swept concave (R20). The v1.2 straight side stopped the yoke at +48°;
  curls and flies need up to +95°. Free swing is now −81° to +103°. Strength: level with or slightly above the standard plate
  (100 lb cable: static 4.4, fatigue 1.6); rating unchanged at 75 lb.
- **Docs:** BOM (R8 from Amazon, bronze sleeve from McMaster-Carr), print settings, safety factors, build order.
- **Files renamed** `yeti-paw-v1.2-*` → `yeti-paw-v1.3-*`. The v1.2 files are attached to the v1.2 release.

## Research v2.0 — 2026-10-17

`research/yeti-paw-handle-research.pdf`, 31 pages.
- Four movements instead of one: lateral raise, bicep curl, Bayesian curl, chest fly, each with its lifter figure.
- Cable source: a Voltra on a 45° rack bracket, cable exit 8 in. off the floor (raise and curls); a flush-mounted pair just
  below shoulder height (fly). The lateral raise's hardest point moves from 33° to 44°.
- New front matter (bottom line, contents, resistance curves for all four movements) and a hardware section (plate strength,
  yoke swing per movement, eye sleeve, orientation check).
- Same design as v1.0: black band, gym red, Barlow Condensed headings, IBM Plex text.

## Research v1.0 — 2026-10-16

The lateral-raise design study (7 pages): standard vs centered pivot, 18 in. low pulley. Attached to the `research-v1.0`
release.

## Hardware v1.2 — Oct 2026

Carabiner yoke with a 3 mm radius on every edge at 100 % infill; YETI STRENGTH painted on the yoke; one Bambu project per
print; anti-curl plate settings; bearing seats opened up 0.05 mm; safety factors re-run (rating 75 lb). The centered-pivot
side plates were added as an optional variant.

## Hardware v1.1 — Oct 2026

First public release: tangent-arc side-plate outline, PAW logo, supports for the bearing seats, safety factors on this geometry.
