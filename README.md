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
