# Bin Enclosure & Stand — Parametric 3D Model

An interactive, parametric 3D model of the HDPE bin enclosure and aluminium stand described in **`Fabrication_Order_Sheet_Enclosure_and_Stand_VENDOR_ISSUE_07.docx`** (see `docs/`).

Every dimension in the model is a named, editable parameter traced back to the fabrication sheet's own section numbers (§1 Enclosure, §2 Internal Parts, §3 Stand & Base Plate). Changing a parameter regenerates all dependent geometry automatically — wall positions, clear widths, hole offsets, hinge pivots, etc.

## Open it

Just open **`index.html`** in a browser (Chrome/Firefox/Edge, desktop). No build step, no install — it loads Three.js from a CDN and runs entirely client-side.

You can also open it via GitHub Pages once enabled for this repo (Settings → Pages → deploy from `main` / root), or double-click the file locally.

## What's in the model

- **§1 Bin Enclosure (outer shell)** — base panel, side/back walls, welded upper front panel (with its 2× Ø16 mm holes), hinged top lid, hinged lower access door, internal divider.
- **§2 Internal mechanical parts** — tilting flap (±40°), dry & wet waste caddies.
- **§3 Stand & base plate** — aluminium support pole, base flange, plywood base plate, plus an illustrative monitor mount on the pole (see note below).

## Controls

- **Iso / Front / Side / Top** view presets, plus free orbit / pan / zoom (drag, right-drag, scroll).
- **Cutaway** — hides the right wall / front panels / door / lid so you can see inside.
- **Labels** / **Dimensions** toggles.
- **Exploded offset** and **Transparency** sliders.
- Every dimension in the left sidebar is a live slider grouped by fabrication-sheet section.

## Exports

- **Export Params (JSON)** — the current parameter set, plus derived values (clear width, door clearance, etc.).
- **Export CAD Model (.scad)** — an [OpenSCAD](https://openscad.org/) file using the same named variables, so the geometry can be opened, edited, and further built on in a real CAD tool.

## Known ambiguities / assumptions

The fabrication sheet does not fully dimension everything. Anything the model can't trace to a spec line is flagged with a ⚠ warning marker in the sidebar and listed in the in-app "Ambiguities & Assumptions" panel, including:

- Hole spacing on the upper front panel (only "centered horizontally" is given).
- The base flange's actual geometry (the sheet explicitly leaves this to the vendor to propose) and its bolt-circle diameter.
- The internal divider's thickness (assumed = 5 mm HDPE sheet stock used elsewhere).
- **Layout**: the bin is a free-standing unit, not mounted on the pole — the sheet gives no attachment between them. The stand instead carries a **monitor** (not mentioned in the fabrication sheet at all), fed by a cable routed through the pole's two grommet holes. The monitor's size and mounting height are illustrative placeholders, not from the source document.

Do not fabricate directly from any parameter marked ⚠ — confirm with the vendor first.

## Source

Fabrication Order Sheet — Enclosure & Stand, Vendor Issue 07 (`docs/`).
