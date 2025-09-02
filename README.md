# Hole_Inner QGIS Plugin

**Hole_Inner** is a QGIS plugin that lets users digitize either a *hole* (cut-out) inside an existing polygon or an *inner* (independent) polygon inside a parent polygon. It supports snapping, preview, and is designed to be undo-friendly when used inside QGIS edit sessions.

## Features
- Create a hole (cut out) from a selected parent polygon.
- Create an inner (standalone) polygon inside a parent polygon.
- Snapping support and preview while digitizing.
- Undo-friendly: designed to work within QGIS editing framework.

## Requirements
- QGIS 3.x (tested with 3.16+).
- A polygon vector layer enabled for editing and set as the active layer.
- **No external Python dependencies** (pure PyQGIS and standard library).

## Installation (for testing)
1. Download the ZIP and extract the folder `Hole_Inner` into your QGIS plugins directory (on Windows typically `%APPDATA%\QGIS\QGIS3\profiles\default\python\plugins\`).
2. Restart QGIS and enable the plugin from `Plugins > Manage and Install Plugins`.
3. Open a polygon layer, toggle editing, and activate the Hole_Inner tool from the toolbar or Plugins menu.

## Quick usage
1. Start editing on your target polygon layer (the parent polygon layer).
2. Activate the plugin tool (toolbar or Plugins menu).
3. Digitize a polygon inside the parent polygon. Choose whether to create a *Hole* or an *Inner* polygon in the plugin options.
4. Save edits to apply changes.

## Test data
A small sample GeoJSON file `test_data.geojson` is included for quick testing (2 polygons). Load it into QGIS and use the plugin to create holes or inner polygons within the sample features.

## Notes for publishing
- License: GPL-3 (included as `LICENSE.txt`).
- Repository: https://github.com/oseyiajibare/Hole_inner
- Tracker: https://github.com/oseyiajibare/Hole_inner/issues

---

Original README content (kept below):

```
Hole vs Inner Polygon Detection - Advanced Plugin
-----------------------------------------------------------
Version: 1.2
Author: Seyi Ajibare

Features (advanced prototype):
- Contextual menu (Create Hole / Add Inner Feature / Options) when starting inside a polygon.
- Options dialog (default mode, snapping toggle, confirmation before commit) stored via QSettings.
- Improved live preview with translucent fill and vertex marker.
- Attribute mapping dialog for inner features (pre-fills from parent feature where possible).
- Basic undo-friendly behavior using layer edit sessions (startEditing / commitChanges / rollBack).
- Logging of actions in plugin memory (plugin.tool.log).
- Includes icon.svg (vector) and icon.png placeholder. Please replace icon.png with a real PNG if desired.

Installation:
1. Unzip the folder into your QGIS plugins directory (or copy the folder).
2. Restart QGIS and enable the plugin from Plugins > Manage and Install Plugins.
3. Use the toolbar icon or the plugin menu to activate the tool.

Notes & recommended production improvements:
- Integrate with QGIS Edit Command / UndoStack for per-action undo/redo (requires using QgsEditCommand classes).
- Add snapping to parent boundary using QgsSnappingUtils for precise vertex placement.
- Improve attribute form to support types, dropdowns and value validation.
- Provide a preferences panel to choose which layers to target and to customize colors/styles.
- Add unit tests and sample layers for QA.

```
