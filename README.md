# Hole vs Inner Polygon Tool (QGIS Plugin)

## 📌 Overview
This QGIS plugin improves polygon digitizing workflows by allowing users to easily choose whether a new polygon inside an existing one should:
- 🕳️ Become a **hole** (subtracting area)
- 🧱 Become an **inner feature** (independent geometry inside parent)

It provides real-time previews, smart defaults, and an undo-friendly workflow.

---

## ✨ Features
- **Contextual Menu**: Choose "Create Hole" or "Add Inner Feature" after drawing.
- **Smart Defaults**: Suggests hole if touching boundary, inner feature if fully inside.
- **Live Preview**: 
  - 🔴 Red = invalid geometry  
  - 🔵 Blue = hole  
  - 🟢 Green = inner feature
- **Undo-Friendly**: Every action can be reverted with `Ctrl+Z`.
- **Attribute Linking**: Inner features can inherit attributes from parent polygon.

---

## 🛠 Installation
1. Download the latest release as a `.zip` from [Releases](https://github.com/oseyiajibare/Hole_inner/releases).
2. In QGIS, go to **Plugins → Manage and Install Plugins → Install from ZIP**.
3. Select the downloaded file and click **Install Plugin**.
4. Activate it via **Plugins → Hole vs Inner Polygon Tool**.

---

## 🚀 Usage
1. Select a polygon layer.
2. Click inside an existing polygon.
3. A menu appears with:
   - 🕳️ **Create Hole**
   - 🧱 **Add Inner Feature**
4. Confirm and the geometry updates instantly.

---

## 📷 Icon
The plugin includes a simple icon (`icon.png`) for toolbar visibility.

---

## 📜 Metadata
See [metadata.txt](metadata.txt) for plugin details.

---

## 🧑‍💻 Development
Clone the repo and copy the folder into your QGIS plugins directory:
- **Linux:** `~/.local/share/QGIS/QGIS3/profiles/default/python/plugins/`
- **Windows:** `C:\Users\<USER>\AppData\Roaming\QGIS\QGIS3\profiles\default\python\plugins\`
- **Mac:** `~/Library/Application Support/QGIS/QGIS3/profiles/default/python/plugins/`

---

## 🐞 Issues
Report bugs or request features here:  
👉 [GitHub Issues](https://github.com/oseyiajibare/hole_inner_plugin/issues)

---

## 📄 License
Hole vs Inner Polygon Tool (QGIS Plugin)
Copyright (C) 2025 Seyi Ajibare

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
