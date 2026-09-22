# Bin Enclosure & Stand — Parametric 3D Model

An interactive, parametric 3D model of the HDPE bin enclosure and aluminium stand described in **`Fabrication_Order_Sheet_Enclosure_and_Stand_VENDOR_ISSUE_07.docx`** (found in `docs/`).

Every dimension in the model is a named, editable parameter traced back to the fabrication sheet's section numbers (§1 Enclosure, §2 Internal Parts, §3 Stand & Base Plate). Changing any parameter automatically regenerates all dependent geometry — wall positions, clear widths, hole offsets, hinge pivots, and clearances.

---

## 🚀 How to Open the 3D Model

You do **not** need to install anything, configure dependencies, or run a build step. The model runs client-side in any modern web browser (Chrome, Edge, Firefox, Safari, Brave).

### Method 1: Double-Click (Quickest & Simplest)
1. Open this repository folder on your computer.
2. Locate the file named **`index.html`**.
3. **Double-click** `index.html` (or right-click → **Open with** → **Google Chrome**, **Microsoft Edge**, or **Firefox**).
4. The interactive 3D viewer will immediately launch in your browser!

---

### Method 2: Live Online via GitHub Pages (No Download Needed)
You can view this 3D model directly on the web using GitHub Pages:

1. Go to your GitHub repository: [https://github.com/siansusan/dustbin](https://github.com/siansusan/dustbin)
2. Click **Settings** (top tab) → select **Pages** from the left sidebar.
3. Under **Branch**, select `main` and keep folder as `/(root)`, then click **Save**.
4. Within 1–2 minutes, your model will be live at:  
   👉 **`https://siansusan.github.io/dustbin/`**

---

### Method 3: Using a Local Web Server (Optional)
If you prefer running a local development server:

- **Using Python**:
  ```bash
  python -m http.server 8000
  ```
  Then navigate to [http://localhost:8000](http://localhost:8000) in your browser.

- **Using Node / npx**:
  ```bash
  npx serve .
  ```

- **Using VS Code**:
  Install the **Live Server** extension, right-click `index.html`, and choose **"Open with Live Server"**.

---

## 🎮 How to Use & Interact with the 3D Model

### Navigation Controls
| Action | Mouse | Trackpad |
| :--- | :--- | :--- |
| **Rotate / Orbit** | Left-click + drag | One-finger click + drag |
| **Pan (Move Camera)** | Right-click + drag | Two-finger click + drag |
| **Zoom In / Out** | Scroll mouse wheel | Two-finger pinch / spread |

### Top Toolbar Features
- **Preset Camera Views**: Click **Iso**, **Front**, **Side**, or **Top** for instant orthogonal and perspective alignments.
- **Cutaway**: Hides outer panels and doors so you can inspect internal parts (divider, waste caddies, tilting flap).
- **Labels**: Toggles floating part names in 3D space.
- **Dimensions**: Toggles live dimension callouts in centimetres.
- **Export CAD Model (.scad)**: Generates and downloads an [OpenSCAD](https://openscad.org/) parametric CAD file ready for editing or 3D fabrication.
- **Export Params (JSON)**: Exports all active dimensions and derived clearances as a JSON file.

### Left Sidebar Controls
- **Adjust Dimensions**: Expand any section (§1 Enclosure, §2 Internal Parts, §3 Stand) to adjust sliders for heights, widths, angles, and sheet thicknesses in real time.
- **Hinged Motion**: Adjust the **Door open angle** (0°–110°) and **Lid open angle** (0°–100°) sliders to check physical clearance and opening paths.
- **Flap Tilt**: Test the ±40° tilting waste flap mechanism.

---

## 📦 What's in the Model

- **§1 Bin Enclosure (Outer Shell)**: Base panel, side/back walls, welded upper front panel (with 2× Ø16 mm holes), hinged top lid, hinged lower access door, and internal divider.
- **§2 Internal Mechanical Parts**: Tilting flap (±40°), dry & wet waste caddies.
- **§3 Stand & Base Plate**: Aluminium support pole, base flange, plywood base plate, plus an illustrative pole-mounted monitor mount.

---

## ⚠ Known Ambiguities & Assumptions

The original fabrication sheet leaves several details open to vendor proposal. Parameters marked with **⚠** in the sidebar are assumptions and include:
- **Hole Spacing**: Upper front panel holes are centered horizontally as specified, with spacing assumed at 8 cm.
- **Base Flange**: Vendor-proposed geometry and bolt-circle diameter.
- **Internal Divider Thickness**: Assumed at 5 mm HDPE sheet stock matching other panels.
- **Bin / Stand Relationship**: The bin is a free-standing unit beside the pole stand (the sheet specifies no physical fasteners between the bin and the stand). The stand carries a monitor fed by internal pole cabling.

> [!WARNING]
> Do not fabricate parts directly from any parameter flagged with ⚠ without verifying with the vendor/order sheet first.

---

## 📄 Source Document
Fabrication Order Sheet — Enclosure & Stand, Vendor Issue 07 (available in [`docs/Fabrication_Order_Sheet_VENDOR_ISSUE_07.md`](docs/Fabrication_Order_Sheet_VENDOR_ISSUE_07.md)).

