# TART Array Structure

CAD files for the mechanical structure of the [TART (Transient Array Radio Telescope)](https://tart.elec.ac.nz/) antenna array — an open-source, low-cost radio telescope built from arrays of small antennas.

This repository contains the full set of design files needed to build the array structure: the master FreeCAD design, flat-pack cutting files (DXF) for CNC machining, 3D-printable parts (STL/3MF), and the FreeCAD source files for each component.

## Repository Layout

```
array-structure/
├── array-design.FCStd          # Master FreeCAD design of the spiral array structure
├── array-design.dxf            # 2D export of the array design
├── array-design.stp            # STEP (3D CAD exchange) export of the array design
├── spiral-array-screenshot.png # Render of the array
├── spiral-array-screenshot-2.png
├── brackets/                   # Brackets for mounting the array arms
├── cam-files/                  # CNC/laser/water-jet cutting files for plywood sheets
├── supports/                   # Stand support structures
└── truss_tube_support/         # Truss-tube support structure (3D-printable)
```

## cam-files/ — Plywood Cutting Files

Files for CNC cutting the flat-pack array structure from sheets of marine-grade exterior plywood. Each file is a full 2400 × 1200 mm sheet, and includes a marked 100 × 100 mm reference square for the workshop to calibrate dimensions against.

| File | Material |
|------|----------|
| `tart_array_4mm_sheet_1.dxf` | Full sheet 2400 × 1200 mm, 4–6 mm plywood |
| `tart_array_4mm_sheet_2.dxf` | Full sheet 2400 × 1200 mm, 4–6 mm plywood |
| `tart_array_9mm.dxf` | Full sheet 2400 × 1200 mm, 9–12 mm plywood |

SVG versions are also provided. The sheets can be cut by laser or water-jet (both are unlikely to shift the material during cutting).

## brackets/ — Mounting Brackets

FreeCAD (`*.FCStd`) designs for the brackets that join the array components:

- `centre to post bracket.FCStd` — connects the array centre to the support post
- `post to arm bracket.FCStd` — connects the support post to the array arms
- `post to arm bracket-Post side bracket.3mf` — 3D-printable export of the post-side bracket

## supports/ — Stand Supports

- `StandFoot.FCStd` — stand foot designed for a 30 mm PVC pipe to serve as the stand leg.

## truss_tube_support/ — Truss Tube Support Structure

A truss-tube support structure design by **Shoaib Mirza** (shoaibmirza@iub.edu.bd), Independent University, Bangladesh, developed for the Bangladesh TART installation.

- `STLs/` — 16 3D-printable parts (STL, binary) covering the full assembly:

  | Group | Parts |
  |-------|-------|
  | Center Hub Assembly | `HUB-001` (top), `HUB-002` (middle), `HUB-003` (bottom) |
  | Joint Assembly | `JNT-001` base joint, `JNT-002`/`JNT-003` top joint parts A/B |
  | Stand Leg Assembly | `LEG-001`–`LEG-004` (parts A–D) |
  | Mount Assembly | `MNT-001` wing mount, `MNT-002`/`MNT-003` top secondary mount parts A/B |
  | Wing Assembly | `WNG-001` (top), `WNG-002` (middle), `WNG-003` (bottom) panels |

- `BOM_STL_Export.csv` — bill of materials listing every part, its assembly group, file name and format
- `full_assembly_step/truss_tube_tart.step` — full assembly as a STEP file
- `renders_and_drawings/START_stand_drawing_v4.pdf` — drawing of the stand

## Building Your Own Array

The DXF cutting files for the current array design live in the `cam-files/` directory (see the cam-files [README](cam-files/README.md) for details). All files in this repository are open — download, cut or print, and assemble.

## Videos

Build and installation guides on YouTube for the TART array structure:

| Video | Channel | What it covers |
|-------|---------|----------------|
| [The Structure of the TART Spiral Antenna Array](https://www.youtube.com/watch?v=TuFPHJMHvuQ) | TART Radio Telescope | How the spiral array is constructed from 3 layers of flat material, plus mounting it on site — the closest match to the `cam-files/` plywood sheets in this repo |
| [How to Build a Cheap Radio Telescope (TART Single Sheet)](https://www.youtube.com/watch?v=K_8zffsw-ng) | TART Radio Telescope | Full build of the simplest TART version from a single standard-size plywood sheet using off-the-shelf components |
| [Single Sheet Radio Telescope Antenna Array Construction](https://www.youtube.com/watch?v=15vWiKbK2I0) | Elec Research | How to make a simple single-sheet TART antenna array with easily available tools and materials |
| [Installing a Spiral TART Using Wooden Posts](https://www.youtube.com/watch?v=bsTKXGvduMo) | TART Radio Telescope | On-site installation: locating the posts that support each arm and making the final arm assembly — relevant to the `brackets/` and `supports/` designs |
| [Single Sheet TART Antenna Array Optimization](https://www.youtube.com/watch?v=b-6-I6850Wc) | Elec Research | Evolution of the antenna layout constrained to a single sheet of plywood — background on the `cam-files/` design |
| [The Transient Array Radio Telescope (TART) – Stanley Kuja](https://www.youtube.com/watch?v=hKns6zeaH-c) | SARAO Web | Overview talk introducing the TART telescope |

More videos, including the "How to Build a Cheap Radio Telescope" series, are on the official [TART Radio Telescope YouTube channel](https://www.youtube.com/@TARTRadioTelescope).

## License / Credits

- Truss-tube support structure: Shoaib Mirza (Independent University, Bangladesh).
- See the `truss_tube_support/README.md` for details.
