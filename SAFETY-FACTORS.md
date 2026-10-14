# YETI PAW v1.2 — Safety factors

Designed by **Schnibbz** · YETI STRENGTH

## Rating: 75 lb working load

**Rated working load: 75 lb (34 kg)** on the cable, for repeated reps.

**Not physically load-tested.** The rating comes from analysis only (below); no unit has been proof-loaded.

## Results

The weakest parts are the **carabiner yoke** and the **pad dowel**, about equal. The side plates have more margin.

| Cable load | Yoke — static | Yoke — fatigue | Side plate — static | Side plate — fatigue | Pad dowel — static | Pad dowel — fatigue |
|---|---|---|---|---|---|---|
| 50 lb (23 kg) | 7.0 | 2.4 | 8.3 | 2.9 | 6.9 | 2.4 |
| **75 lb (34 kg, rated)** | **4.6** | **1.6** | **5.5** | **2.0** | **4.6** | **1.6** |
| 100 lb (45 kg, above rating) | 3.5 | 1.2 | 4.1 | 1.5 | 3.5 | 1.2 |

**How to read it.** A safety factor (SF) is how many times stronger the part is than the stress it sees. SF 2 means it would
take twice the load to reach the limit.
- **Static** is for a single pull. Could one rep at this load break it?
- **Fatigue** is for many reps, on the order of a million. Could thousands of sessions at this load wear a crack into it?
  This is the one that matters for training, and it sets the rating.

**Why 75 lb.** At 75 lb the lowest fatigue SF is 1.6 (yoke and pad dowel), above the 1.5 minimum used here for repeated
loading. v1.2's stronger yoke adds margin at the same rating; it does not raise the rating.

**Why the 100 lb row is shown.** It shows how quickly the margin disappears: one pull at 100 lb is still inside static
strength (SF 3.5 or more), but the fatigue SF of the yoke and dowel drops to 1.2, which leaves no real margin for repeated
use. **Do not use it above
75 lb.** The 100 lb row is not an allowance.

## How these numbers were made

- **Model:**
  - Side plate and yoke: 2D plane-stress finite-element analysis (both are flat parts loaded in their own plane), about
    50–75 k nodes each.
  - Pad dowel: hand calculation of bending across its length plus the D-stub ends. It prints upright, so this load runs
    ACROSS the layers and uses the weaker layer-to-layer strength (38 MPa).
- **Load cases:**
  - Plate: the cable force arrives at the yoke pivot from any direction (12 directions checked). It is reacted either at the
    handle or at the wrist pad, and the worst case is reported.
  - Yoke: the pull is along the yoke and ±30° off it.
  - Each plate carries half the cable force (assumed equal split).
- **Stress:** von Mises, 99.5th percentile, which ignores single-point mesh spikes. Real peak stresses right at hole edges
  may be higher than shown, and fatigue cracks start there. That is one reason the fatigue margin, not the static one, sets
  the rating.
- **Material:** ELEGOO PETG-CF: 51 MPa along the layers, 38 MPa across them. The plate and yoke print flat, so their load
  runs along the layers.
- **Knock-downs:**
  - × 0.75 for printed walls and infill on the side plates: **6 walls, 40 % gyroid**;
  - × 0.90 for the yoke, printed at **100 % infill**: the material's test bars are themselves printed solid, and 0.90 keeps
    some margin for gaps between printed lines;
  - the yoke's 3 mm edge radius removes material at the corners of its 18 × 12.7 mm band. A 2D model can't show an edge
    radius, so the yoke's stresses are increased by 9.6 % (the loss in bending strength of that section);
  - × 0.35 for fatigue, a rule of thumb for polymers at about a million cycles.
- **Not modelled:**
  - print defects and poor layer bonding;
  - wet filament;
  - impact, such as dropping the stack or a cable snapping back;
  - heat (car interiors, direct sun);
  - UV ageing;
  - wear of the bearings and sleeves.

**These figures only apply if you print as specified.** Use PETG-CF, the walls and infill above, and dried filament (see
[PRINT-SETTINGS.md](PRINT-SETTINGS.md)). Other materials, fewer walls, lower infill or a different orientation will be weaker.
**Never print it in PLA**: PLA creeps under steady load and softens in a hot car.

## Inspect before every session

Check the yoke, especially around the two pivot bosses and the carabiner eye, and the side plates around all three holes.
Also check the dowel's D-shaped ends and its threads.
**Stop using it** at the first sign of whitening (stress marks), cracks, new play in the pivots, or a bearing that has moved.
**Reprint the yoke** after any drop or impact, and at any whitening.

---

**Not professionally engineered.** The Yeti Paw was designed by a hobbyist, not by a licensed or qualified engineer. These
safety factors are amateur estimates from a simplified computer model. They are not a certified load rating and come with no
guarantee.

**Build and use at your own risk.** You are responsible for printing, assembling, inspecting and using this device. Print
quality, materials, settings and assembly vary, so your parts may be weaker than described. The designer accepts no liability
for injury or damage arising from building or using it.
