# YETI PAW v1.3 — Safety factors, centered-pivot side plates

Designed by **Schnibbz** · YETI STRENGTH

This page covers the **optional centered-pivot side plates** (the yoke hole centered between the handle and the pad,
85 mm to each; in v1.3 the side between the yoke and the handle is swept concave (R20) so the yoke can follow the cable on curls
and flies). Everything else in the build is unchanged, so the yoke and pad dowel figures are the same as on the main
[Safety factors](SAFETY-FACTORS.md) page.

## Rating: 75 lb working load (unchanged)

**Rated working load: 75 lb (34 kg)** on the cable, for repeated reps.

**Smart cable machines can be set far above the rating.** A Voltra I, for example, goes up to 200 lb. Keep the setting at or below 75 lb.

**Not physically load-tested.** The rating comes from analysis only (below); no unit has been proof-loaded.

## Results

| Cable load | Yoke — static | Yoke — fatigue | Centered plate — static | Centered plate — fatigue | Pad dowel — static | Pad dowel — fatigue |
|---|---|---|---|---|---|---|
| 50 lb (23 kg) | 7.0 | 2.4 | 8.9 | 3.1 | 6.9 | 2.4 |
| **75 lb (34 kg, rated)** | **4.6** | **1.6** | **5.9** | **2.1** | **4.6** | **1.6** |
| 100 lb (45 kg, above rating) | 3.5 | 1.2 | 4.4 | 1.6 | 3.5 | 1.2 |

The yoke and the pad dowel are still the weakest parts. The centered plate has more margin than either, so it does not
change the rating.

**Centered plate vs standard plate, side by side.** Both plates were run through the same analysis with the same mesh
settings, so their numbers compare directly:

| Cable load | Standard plate — static | Standard plate — fatigue | Centered plate — static | Centered plate — fatigue |
|---|---|---|---|---|
| 50 lb | 8.7 | 3.1 | 8.9 | 3.1 |
| **75 lb** | **5.8** | **2.0** | **5.9** | **2.1** |
| 100 lb | 4.4 | 1.5 | 4.4 | 1.6 |

The centered plate (v1.3, R20 sweep) matches the standard plate within the same 2D check (identical static factors; the 1.5 vs 1.6 fatigue difference is rounding). The yoke and the pad dowel, not the plate, remain the weakest parts. (The v1.2 centered plate,
with a straight yoke-to-handle side, was about 5 % stronger but stopped the yoke at +48°, too little for curls and flies.) The standard plate's numbers here differ slightly from the
main page because the main page used a finer mesh; the comparison above uses the same settings for both.

**Where it is highest.** The worst case for the centered plate is the load reacted at the handle, next to the R20 sweep. For the standard plate
it is the load reacted at the handle. The centered plate also uses about 24 % less plastic (75 vs 99 cm³ before the edge
radius).

**How to read it.** A safety factor (SF) is how many times stronger the part is than the stress it sees. SF 2 means it would
take twice the load to reach the limit.
- **Static** is for a single pull.
- **Fatigue** is for many reps, on the order of a million. This is the one that matters for training, and it sets the rating.

**Do not use it above 75 lb.** The 100 lb row is not an allowance.

## How these numbers were made

Same method as the main page:
- **Model:** 2D plane-stress finite-element analysis of the plate (a flat part loaded in its own plane), about 24 k nodes,
  with every boundary resampled at the same 1 mm spacing for both plates so the two meshes match.
- **Load cases:** the cable force arrives at the yoke pivot from any direction (12 directions checked) and is reacted either
  at the handle or at the wrist pad; the worst case is reported. Each plate carries half the cable force.
- **Stress:** von Mises, 99.5th percentile, which ignores single-point mesh spikes. Real peak stresses right at hole edges
  may be higher than shown.
- **Material:** ELEGOO PETG-CF, 51 MPa along the layers (the plate prints flat, so the load runs along the layers).
- **Knock-downs:** × 0.75 for printed walls and infill (**6 walls, 40 % gyroid**); × 0.35 for fatigue.
- **Yoke swing:** checked on the final plate shape. The yoke swings freely from −81° to +103°. With the cable from a Voltra
  8 in. off the floor, the movements need: lateral raise −41° to +29°, bicep curl −37° to +92°, Bayesian curl −50° to +95°;
  chest fly (cables just below shoulder height) −47° to +75°. These are covered at the modeled stances. With the cable
  closer behind you (a Bayesian curl with the Voltra about 20 in. behind the shoulder or the upper arm 35° back, or a fly
  with the cable exits close behind the shoulders) the yoke needs up to +110° to +122° in the first few degrees of the rep,
  so it reaches its +103° stop and bears on the plate edge under the full cable load. Inspect that edge, and stand a little
  further from the Voltra for those movements.
- **Not modelled:** print defects and poor layer bonding, wet filament, impact, heat, UV ageing, bearing and sleeve wear,
  and the bearing seats cut into the plate (the 2D model treats the plate as a full 10 mm thick).

**These figures only apply if you print as specified** (see [PRINT-SETTINGS.md](PRINT-SETTINGS.md)): PETG-CF, dried, 6 walls,
40 % gyroid, plate printed flat. Other materials are untested here. **Never print it in PLA.**

## Inspect before every session

Check the side plates around all three holes, the yoke around its pivot bosses and carabiner eye, and the dowel's ends and
threads. **Stop using it** at the first sign of whitening (stress marks), cracks, new play in the pivots, or a bearing that has
moved.

---

**Not professionally engineered.** The Yeti Paw was designed by a hobbyist, not by a licensed or qualified engineer. These
safety factors are amateur estimates from a simplified computer model. They are not a certified load rating and come with no
guarantee.

**Build and use at your own risk.** You are responsible for printing, assembling, inspecting and using this device. Print
quality, materials, settings and assembly vary, so your parts may be weaker than described. The designer accepts no liability
for injury or damage arising from building or using it.
