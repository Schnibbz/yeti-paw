# YETI PAW v1.2 — Print settings (any printer)

These are the v1.2 settings, used on a Bambu X1C. Bambu users can open the three projects, which have everything below
already set and painted:
[side plates](https://github.com/Schnibbz/yeti-paw/raw/main/yeti-paw-v1.2-plates-PROJECT.3mf) (both on one bed),
[yoke](https://github.com/Schnibbz/yeti-paw/raw/main/yeti-paw-v1.2-yoke-PROJECT.3mf) and
[pad dowel](https://github.com/Schnibbz/yeti-paw/raw/main/yeti-paw-v1.2-dowel-PROJECT.3mf). On any other printer or slicer (PrusaSlicer, OrcaSlicer, Cura, …), use the files in
[`stl/`](stl/) and copy these values. The STLs are already in print orientation.

**Strength depends on these settings.** The safety factors assume **6 walls and 40 % gyroid** in PETG-CF on the plates, and
**100 % infill** in the yoke and the dowel. Printing lighter makes the parts weaker than stated.

## Material and printer

| Item | Setting |
|---|---|
| Body | **PETG-CF** (carbon-fibre PETG). Tested with ELEGOO PETG-CF: 51 MPa X-Y / 38 MPa Z. |
| Logo | White PETG (SUNLU), about 18 g per Yeti Paw (both plates) |
| Nozzle | **0.4 mm hardened steel**: CF wears out brass |
| Dry the filament | 65 °C for 8–10 h before printing. Wet PETG strings and bonds poorly. |
| Bed | **Textured PEI: 75 °C** for the side plates and the yoke, 70 °C for the dowel. It gives the outer face its texture. Smooth PEI or glass also work, with glue stick as a release agent. |
| Nozzle temp | PETG-CF **255 °C**; white PETG 250 °C |
| Flow | Calibrate it per spool. Mine: PETG-CF 0.99, white PETG 0.95 |
| Max volumetric speed | PETG-CF 11.5 mm³/s; PETG 12 mm³/s |
| Cooling | Fan off for the first 3 layers, then 5–40 %; **80 % on overhangs** steeper than 25 %. Minimum layer time 6 s. |

## Part by part

| Part | Orientation | Infill | Supports | Time (X1C) |
|---|---|---|---|---|
| Side plate L and R | **Outer face DOWN** (the logo face is on the bed). Both on one bed. | 6 walls, 40 % gyroid | See below | ≈ 7.7 h for the pair |
| Centered-pivot side plates L and R (variant) | Same as the side plates | Same | Same | ≈ 6.6 h for the pair |
| Carabiner yoke | **Flat, band face down**. The eye's flange pocket faces UP. | 6 walls, **100 %** (rectilinear) | Under the two pivot bosses only, **none inside the Ø12 pivot bores**. See below. | ≈ 2.8 h |
| Pad dowel | **Upright**, standing on one end | **100 %** (rectilinear) | **Under the shoulder** where the Ø25.4 body overhangs the bottom D-stub, about 10 mm up. Support body in PETG-CF, **the 3 interface layers in PLA at zero gap**. PLA doesn't bond to PETG, so the shoulder prints flat and the support peels off clean. **None in the threaded holes.** 5 mm brim. | ≈ 3.9 h |

## Yoke — the details that matter

**Bambu users:** print the yoke from
[`yeti-paw-v1.2-yoke-PROJECT.3mf`](https://github.com/Schnibbz/yeti-paw/raw/main/yeti-paw-v1.2-yoke-PROJECT.3mf). It holds
the exact settings below, which have been printed and checked.

**YETI STRENGTH** is painted white on the yoke's bed face, the same way as PAW on the plates. The model has a 0.02 mm step
where the letters are, so the slicer's paint has an edge to follow. It's far too shallow to print, so it costs no strength.
About 1 mm of white (5 layers).

Every edge of the yoke has a 3 mm radius, including the round pivot bosses where they curve down to the bed. Tested on
PETG-CF: support the **flat bottom of each boss only**. Up the steeper part of the curve, PETG prints on its own, and any
support there fuses to the part and tears it on removal.

| Setting | Value |
|---|---|
| Where to support | Painted enforcers **only under the flat bottom of each pivot boss**: the part tilted more than 45° from vertical, about the first 3 mm. Also the **rounded ends** of each boss (the 3 mm radius where the end faces curve down to the bed), out to 60° from vertical, about 5 mm up. Block everything else, including the Ø12 bores and the 3 mm radius along the bottom edge. Turn off "remove small overhangs" so the small end patches aren't dropped. |
| Support style | **Snug**, not grid |
| Top Z distance | **Exactly one layer**: 0.2 mm at 0.2 mm layers. Some slicers round the gap to whole layers, so 0.3 becomes 0.4. |
| XY distance | 0.35 mm |
| Top interface | **4 layers, 0.10 mm spacing, concentric pattern, ironed**, printed at 40 mm/s |
| Nozzle | **245 °C** for PETG-CF (250 °C first layer) |
| Infill | 100 %, rectilinear (zig-zag) |
| Bed | Textured PEI, **75 °C** |
| Part cooling fan | Off for the first 3 layers, then up to 40 %. **Overhangs 80 %** (above 25 % overhang). |

**Keep the leg tips down.** The yoke is long and its leg tips curl if air blows across them in the first layers:
- leave at least 30 mm between the yoke and the edge of the plate;
- on an enclosed printer with an exhaust or chamber fan, keep that fan off for the first 15 layers (3 mm), then run it at
  30 %. The yoke project does this for you.

## Side plates — the details that matter

Everything in this section applies to the centered-pivot plates too: same settings, same supports, same logo painting.

**Both plates on one bed**, the right plate turned to nest against the left, at least 15 mm from every bed edge and clear of
the X1C's purge lines. **Stop the edges curling:**
- bed **75 °C**;
- **exhaust or chamber fan off until 3 mm**, then 30 %. The project switches it on at that height for you.

With the fan on from the first layer, the plate edges lifted.

**Layers.** 0.2 mm overall, with **0.08 mm layers from 0.2 to 1.32 mm** and **over the top 1.2 mm**. This is a height-range or
variable-layer modifier. The fine layers let the 3 mm edge radius print cleanly on both faces. Keep the first layer at 0.2 mm.

**Edges and walls.**

| Setting | Value |
|---|---|
| Elephant-foot compensation | **0** (the bottom edge is already a radius) |
| Wall order | Inner, then outer |
| Overhang speeds (Bambu's four steps) | 20 / 20 / 15 / 10 mm/s; in other slicers, slow overhangs to 10–20 mm/s |
| Outer wall | 80 mm/s at 2000 mm/s² |
| First layer | 30 mm/s, infill 50 mm/s, 0.5 mm line width |
| Bottom surface pattern | **Monotonic**. Concentric leaves "fingerprints" on the visible face. |
| Bottom shells | 18 layers (about 1.9 mm with the 0.08 mm layers) |
| Top shell | 1.0 mm |

**Supports.** The plate needs support in three places only, all inside the bearing bores:
1. the FR8 flange step, 1.92 mm up in the handle bore;
2. the bearing-seat lip about 8 mm up in the handle bore;
3. the bearing-seat lip about 8 mm up in the yoke (6000) bore.

Use normal / grid supports, not tree:

| Setting | Value |
|---|---|
| Threshold angle | 30° |
| Top Z distance | 0.3 mm |
| XY distance | 0.4 mm |
| Top interface | 3 layers at 0.25 mm spacing |
| Base pattern spacing | 1 mm |

**Block every other overhang** with support blockers: the rounded edges all round the plate and the window would otherwise
fill with support. The holes behind the seat lips are already shaped as "stepped bridges" (slot, then square, then round), so
the lips print flat.

**Seam.** Put it on one aligned line in the concave sweep between the handle and the pad. That edge is the least visible.
Use a scarf seam if your slicer has one.

**PAW logo (two-colour).**
- The PAW letters are a 0.02 mm step in the outer face. It's too shallow to print, but it gives the slicer an edge
  to paint to.
- Paint the letter floors white, with the plate's outer face on the bed.
- Use about **0.8 mm of white**: 8 or more full layers with these settings. Less shows grey from the black behind it.
- Purge generously: black → white about 800 mm³ (CF purges slowly), white → black about 300 mm³.
- Turn on "avoid crossing walls" so the nozzle doesn't drag black across the white.

## After printing

- **Yoke pivot bores:** the roof of each horizontal Ø12 bore sags slightly. Clean the bores back to round with a **Ø12 mm drill
  bit turned by hand**, then press the steel sleeves in.
- **Dowel threads:** they're printed 0.4 mm loose. Run a 1/2"-13 bolt in and out to clean them, with a little wax if it's
  stiff. A bolt with a hacksaw slot cut along its threads works as a tap.
- **Bearing seats** come out tight in a full plate: expect to press the bearings in firmly. Sand the seats lightly rather than
  forcing a bearing that won't start straight.
- Remove the supports from the bearing bores completely, so each bearing seats flat against its ledge.

---

**Not professionally engineered. Build and use at your own risk.** See the disclaimers in the [README](README.md).
