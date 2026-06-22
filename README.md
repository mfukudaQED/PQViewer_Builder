# PQViewer (Builder)

[日本語](README.jp.md) 

---

## Overview

**PQViewer (Builder)** is a WebGL2-based molecular and crystal structure viewer/builder designed to run on GitHub Pages.
It works directly from `index.html` in a browser and provides interactive visualization and editing of structures, volume data, vector fields, and tensor fields.


## Main Features

- **File I/O**
  - Drag-and-drop loading of `xyz`, `cif`, `cube`, `fieldcube`, and `scene json` files
  - Export to `xyz`, `cif`, `scene json`, `PNG`, `OBJ`, `CSV`, and related formats
  - CIF import options for occupancy and disorder handling

- **Structure Visualization and Editing**
  - 3D rendering of atoms, bonds, and unit cells
  - Add, delete, duplicate, replace, move, rotate, mirror, invert, and align atoms
  - Manual bond editing, bond deletion, duplicate-atom merging
  - Cell editing, supercell generation, and periodic display
  - Atom grouping with visibility and opacity controls

- **Rendering and Appearance**
  - Fast WebGL2 rendering
  - Impostor, line, and mesh-like rendering modes
  - Atom labels, bond coloring, outlines, and depth cueing
  - Customizable background, theme, fonts, and accent color
  - PNG export with selectable scale

- **Isosurfaces and Volume Visualization**
  - Isosurface rendering from cube data
  - Positive/negative isosurfaces, opacity, colormaps, and surface coloring by selected color cube
  - Crop, cap, and contour display
  - RCP preset

- **Section / Slice Visualization**
  - Section definition by axis coordinate, point + normal, or three positions
  - 2D scalar maps, contours, ticks, labels, and font settings
  - Atoms and field glyphs on section planes
  - Section colorbars and PNG export
  - MathJax-based text annotations

- **Vector and Tensor Field Visualization**
  - FieldCube loading
  - 3D arrows, lines, tensor principal axes, ellipsoids, stars, astroids, and related glyphs
  - Coloring by magnitude, components, or tensor-derived quantities
  - Clipping, sampling, scaling, and colorbar settings
  - Coupling to the Section Control Panel

- **Lagrange Analysis**
  - Extraction and visualization of Lagrange surfaces
  - Lagrange point search
  - Clipping by density isosurfaces
  - Atom-pair-separated surfaces and surface integration
  - OBJ / CSV export

- **Surface Builder**
  - Miller-index plane preview
  - Slab generation, vacuum settings, and termination analysis
  - Adsorption-site generation, pivot placement, and CSV export

- **Polyhedra Analysis**
  - Coordination polyhedra based on center/ligand elements and cutoff distance
  - Periodic-image-aware analysis
  - OBJ / CSV export

- **Usability**
  - Blender-like and legacy mouse navigation presets
  - Pivot marker, view gizmo, and rotate gizmo
  - Editable shortcut keymap with import, export, and reset
  - UI search, collapsible panels, and resizable plot / section / colorbar areas

## Usage

1. Open `index.html` in a browser.
1. Drag and drop `xyz`, `cif`, `cube`, `fieldcube`, or `scene json` files onto the page or the rendering area.
1. Use the Control Panel to edit structures, generate isosurfaces, create sections, visualize vector/tensor fields, and run Lagrange analysis.
1. Export PNG, XYZ, CIF, OBJ, CSV, or Scene JSON files as needed.

## Example GitHub Pages Layout

```text
repository-root/
├── index.html
├── README.md
└── pqviewer_spglib_wasm_adapter.js   # if used
```

## Requirements

- A modern browser with WebGL2 support
  - Chrome, Edge, Firefox, Safari, etc.
- JavaScript enabled
- Access to the MathJax CDN if mathematical annotations are used

## License

This project is released under the **Mozilla Public License 2.0 (MPL-2.0)**.

MPL-2.0 is a file-level copyleft license. If you redistribute or modify this project, follow the terms of MPL-2.0. When publishing the repository, it is recommended to include a `LICENSE` file.

## Credit

- This Viewer was created using **GPT-5.5**.
- It is implemented with WebGL2, HTML5 Canvas, and JavaScript.
- MathJax is used for mathematical annotations.
