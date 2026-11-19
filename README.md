# MechCompression

**Compression test analyzer for mechanical testing data.** Load raw test files, plot the curves, pick the linear region to get Young's modulus, find the maximum point, and export the results. It all runs in your browser, so your data never leaves your computer.

### ▶ [Open MechCompression in your browser](https://ashif3hq.github.io/MechCompression/)

No installation or sign-up is needed. It works on any modern browser (Chrome, Edge, Firefox, Safari).

---

## Features

- **Opens data from most testing machines**: Instron (Bluehill), ZwickRoell (testXpert), Shimadzu (Trapezium), MTS, Lloyd/NEXYGEN, Tinius Olsen, Testometric, `.TRA` files and plain two- or three-column data, as CSV, TXT, DAT, TSV or Excel (`.xlsx`/`.xls`/`.ods`). The importer auto-detects the delimiter, decimal commas, header and unit rows, column names in English, French, German or Spanish, units (N/kN/lbf/kgf, mm/m/in/µm, s/ms/min), UTF-16 files, and stress–strain-only exports.
- **Reads the specimen dimensions** (diameter, height/gauge length, or width × thickness or area for non-circular specimens) from the file's header when they are present.
- You can load several specimens at once.
- **Three plot views**: stress–strain (σ–ε), force–displacement (F–δ) and force–time (F–t).
- **Young's modulus**: select the linear region on the curve, and the modulus is computed by linear regression, with the fitted line drawn on the curve.
- **Maximum point**: pick the peak stress or force.
- **Specimen parameters**: diameter, length and area per sample, for converting force and displacement to stress and strain.
- **Units**: Pa, kPa, MPa or GPa.
- **Languages**: English, Français, Español.
- **Interactive chart**: pan, box-zoom and reset. You can show or hide each specimen.
- **Graph image export**: publication-ready PNG for reports, theses and slides (300 dpi 4:3, 16:9 slide, square or current view), with a white or transparent background and adjustable text size. You can also copy the graph straight into PowerPoint or Word.
- **Export**: results as CSV or JSON, plus a printable report for each specimen.
- **Dark mode**, collapsible sidebar sections and a built-in sample dataset to try it out.

## Quick start

1. Open the app using the link above.
2. Drop your test files into the sidebar, or click it to browse.
3. Enter the sample ID, diameter and length.
4. Choose a mode: **Young** (click the start and end of the linear region) or **Max** (click the peak).
5. Click **Calculate**, then export to CSV or JSON, or open the report.

## Keyboard shortcuts

| Key | Action |
|---|---|
| `Z` / `P` / `Y` / `M` | Zoom, Pan, Young's modulus, Max σ mode |
| `1` / `2` / `3` | σ–ε, F–δ, F–t view |
| `R` | Reset view |
| `Enter` | Calculate |
| `E` | Export graph image |
| `D` | Toggle dark mode |

## Run locally

Download `index.html` and open it in your browser. You can also serve the folder:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Built with

- [Chart.js](https://www.chartjs.org/) with [chartjs-plugin-zoom](https://www.chartjs.org/chartjs-plugin-zoom/) and Hammer.js
- [Lucide](https://lucide.dev/) icons
- Vanilla HTML, CSS and JavaScript, as a single file with no build step

## Licence

Copyright © 2026 Mohammed Ashif. All rights reserved. See [LICENSE](LICENSE).
