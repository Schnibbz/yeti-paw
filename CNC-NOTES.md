# YETI PAW v1.2 — CNC side plates (machined aluminium)

An option for builders who would rather have the two side plates machined than printed. Everything else stays as in the
main build: the printed yoke and pad dowel, the bearings and the hardware from the [BOM](BOM-yeti-paw.md).

## Files

Send the shop all three:
- [`cnc/yeti-paw-v1.2-plate-left-CNC.step`](cnc/yeti-paw-v1.2-plate-left-CNC.step)
- [`cnc/yeti-paw-v1.2-plate-right-CNC.step`](cnc/yeti-paw-v1.2-plate-right-CNC.step)
- [`cnc/yeti-paw-v1.2-plates-CNC-drawing.pdf`](cnc/yeti-paw-v1.2-plates-CNC-drawing.pdf), which carries the bearing fits,
  depths and notes. A STEP file has no tolerances, so the drawing is what makes the bearings fit.

**Use these, not the files in [`step/`](step/).** Those are the print geometry, with features that only make sense on a 3D
printer.

## What's different from the printed plate

| | Printed plate | CNC plate |
|---|---|---|
| Behind the bearing seats | Stepped slots and squares, so the seat ledge prints without support | Plain counterbores. The stepped shapes have sharp inside corners a mill can't cut. |
| Bearing seat sizes | Tuned for a press fit in printed PETG | Bearing-maker housing fit for aluminium: **K7** |
| Pad D-hole | Sharp corners | Two Ø2 mm corner reliefs, so a Ø2 end mill can cut it and the printed dowel still fits |
| PAW logo | A 0.02 mm step that guides the paint in the slicer | Engraved 0.3 mm deep |
| Edges | 3 mm radius | 3 mm radius, modelled as true fillets |

The outline, the window, the hole positions, the 10 mm thickness and the depth of each seat are the same as the printed
plate.

## Ordering

- **Material:** 6061-T6 aluminium, **10.0 mm** thick. Not 3/8" (9.53 mm): the plate thickness sets the handle stack and the
  fit of the printed dowel.
- **Quantity:** one LEFT and one RIGHT. They are mirror images, not two of the same part.
- **Process:** CNC milling, with two setups because both faces have a 3 mm radius. The bearing seats need an end mill or a
  boring head, so a laser or waterjet cutting service alone can't make these.
- **Cheaper edge option:** a 1 × 45° chamfer instead of the 3 mm radius is acceptable if it saves cost. Ask for it on the
  quote.

## Finishing

The edges matter: these plates are handled and sit against the forearm.

- **Minimum, for everyone:** ask the shop to **break all edges 0.2–0.5 mm, no burrs**. It's a standard request and costs
  little. Without it, expect sharp edges that need hand finishing with a deburring tool and fine abrasive.
- **Recommended:** **bead blast or vibratory tumble**. It gives an even satin finish and softens every edge a little. It
  does not replace the 3 mm radius.
- **Optional:** **anodize Type II** (black looks right), after blasting or tumbling.
- **Protect the bearing seats.** Have the shop mask both seats or hold their sizes after finishing. Anodizing adds material
  and tightens a K7 seat. Keep tumbling media out of the seats.

## Assembly notes for aluminium plates

- **Bearings:** press them from the outer face with an arbor press, pushing on the outer ring only. In aluminium, bearing
  retaining compound (such as Loctite 641) is fine if a seat comes out loose. The no-Loctite rule is for printed PETG.
- **Everything else** follows the README build order.

## Strength

The [safety factors](SAFETY-FACTORS.md) were calculated for PETG-CF printed parts. Aluminium plates are much stronger
than printed ones, but the printed yoke and pad dowel still limit the rating to **75 lb**.

---

**Not professionally engineered. Build and use at your own risk.** See the disclaimers in the [README](README.md).
