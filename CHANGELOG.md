# YETI PAW — Changelog

Two numbered tracks, so a document update never bumps the hardware number:

- **Hardware** (`v1.x`): the printable parts, the parts list, print settings and safety factors. Tags `v1.2`, `v1.3`, …
- **Research** (`research-v1.x`, `research-v2.x`): the handle-design study PDFs. Tags `research-v1.0`, `research-v2.0`, …

Every version is a tagged [GitHub Release](https://github.com/Schnibbz/yeti-paw/releases) with its own files attached, so
older versions stay downloadable. The files in the repo itself are always the latest.

## Hardware v1.3.3 — 2026-10-24

Cosmetic, no part or fit changes.
- **Carabiner yoke: YETI STRENGTH on both faces.** The yoke project now paints the lettering on the top face too, mirrored
  so it reads correctly from that side (same 0.02 mm step method, about 1 mm of white per face, no strength cost). The prime
  tower moved to the open middle of the U, near the bed centre: a tower near the bed edge came loose in testing, and then
  every colour swap purged onto the part. Print time ≈ 3.2 h (was 2.8). Print settings and parts list updated.

## Hardware v1.3.2 — 2026-10-19

Fit change from a printed test, no new parts.
- **Carabiner yoke eye bore Ø22.29 → Ø22.39.** A three-coupon press-fit ladder (Ø22.19 / 22.29 / 22.39) cut from the real
  eye, printed in PETG-CF and pressed with the McMaster 6391K256 bronze sleeve: Ø22.39 gave the right press. The sleeve's
  spec OD (0.877″) alone was too tight in a printed eye. Yoke project, STL, STEP and CNC files updated.

## Hardware v1.3.1 — 2026-10-17

Cosmetic fix, no part or fit changes (same files, same names; v1.3 parts list unchanged).
- **Centered-pivot plates: PAW logo re-centered.** The placement kept 6.5 mm off the bearing holes but only 2.5 mm off the
  window, so the word sat closer to the window (visible gaps 6.2 mm window / 9.5 mm handle hole / 7.7 mm edge). It is now
  placed by the gaps you see: 11.3 mm above, 11.2 mm below, 8.0 mm to the window and 8.0 mm to the handle hole, same
  13.6 mm letters, tilted 16° along the bar, the left plate the mirror of the right. Project, STLs, STEPs and hero updated.

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
  curls and flies need up to +95°. Free swing is now −81° to +103°, which covers all four studied movements at the modeled
  stances; with the cable close behind you (close-stance Bayesian curl or fly) the yoke can still reach the stop in the first
  few degrees of the rep (correction added 2026-10-17 after review). Strength: matches the standard plate within the same 2D
  check (100 lb cable: static 4.4, fatigue 1.6 vs 1.5); rating unchanged at 75 lb; the yoke remains the weakest part.
- **Docs:** BOM (R8 from Amazon, bronze sleeve from McMaster-Carr), print settings, safety factors, build order.
- **Files renamed** `yeti-paw-v1.2-*` → `yeti-paw-v1.3-*`. The v1.2 files are attached to the v1.2 release.

## Research v2.1 — 2026-10-17

`research/yeti-paw-handle-research.pdf`, 34 pages. Revised after an independent critical review of v2.0.
- **Yoke swing** reported as an envelope over every stance checked. The centered plate covers all four movements at the
  modeled stance, but a Bayesian curl with the upper arm 35° back or the cable 20 in. away, and a fly with the cable exits
  8 in. behind the shoulders, take the yoke 7–19° past its stop in the first few degrees of the rep, at full cable tension.
- **New:** small / median / large lifter table (the headline numbers are device geometry plus limb length); peak pad push
  and grip force over the whole rep; where the pad lifts off; wrist moment for all four handles (the centered pivot puts
  roughly 2–4× the current pivot's wrist moment on the wrist at the hardest point, still well under a D-handle's);
  stretched-position cable torque; the cuff comparison over a grid of cuff positions (the ranking flips, so "follows a cuff
  most closely" is gone); handle tilt on the arm (±10°, ±20°), which moves the pad numbers most.
- **Wording:** "+7–16 % more work" → "the same peak at about 6–14 % less weight"; "lifts off" never applied to the hand;
  confidence "on the direction and rough size, not on exact pounds or feel"; offering both variants framed as a hypothesis
  for a lifter trial; strength "matches the original plate within the same check"; rating 75 lb, a Voltra can be set higher.

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
