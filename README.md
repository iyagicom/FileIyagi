# FileIyagi v1.5.0

![FileIyagi](fileiyagi.png)


A **fast and lightweight file manager** for Windows and Linux.

Designed for high responsiveness and stability, especially when handling **Korean text input during file renaming and search**.

Provides fast navigation, keyboard-driven workflow, and smooth thumbnail previews.  
The interface automatically adapts to the system language for a natural user experience.

---

## ✨ Features

### Navigation
* **Breadcrumb Path Bar** — Navigate easily with clickable path blocks
* **Direct Path Input** — Press `Ctrl+L` to edit path (`~` supported)
* **Copy Path** — Click current folder block to copy full path
* **Back / Forward** — Mouse buttons 4·5 or toolbar arrows
* **Favorites Sidebar** — Home, Desktop, Documents + custom bookmarks
* **Devices Section** — Auto-detect drives and USB (Windows/Linux)
* **Auto Mount Detection (Linux)** — Updates on USB connect/disconnect
* **My Devices** — View and mount unmounted drives instantly
* **Recent Files (RECENT)** — Per-folder recent file tracking
* **Path History** — Stores last 15 visited paths (persistent)

### Dual Pane (2-Panel Mode)
* **Toggle Dual Pane** — Status bar ◫ button
* **Restore Last Paths** — Each pane remembers its last location
* **Session Persistence** — Dual pane state preserved after restart

### View
* **Details View** — Name, Size, Type, Date with sorting
* **Icon View** — Small (96px), Medium (150px), Large (224px)
* **Thumbnails** — Auto-generated for images & videos
* **Per-Folder View Memory** — Remembers last view mode
* **Hidden Files Toggle** — `Ctrl+H` or "." button
* **Font Size Control** — `Alt + Wheel` (7–24pt)
* **View Switching** — `Ctrl + Wheel` or `Ctrl+1~4`
* **Quick Sort Buttons** — Name, Size, Type, Date
* **Fixed Columns** — Only Name column is flexible

### Search
* **Always Visible Search Bar**
* **Recursive Search** — Includes subfolders
* **300ms Debounce**
* **Open Files During Search**
* **Drag Search Results**
* **Optimized Layout** — Balanced columns

### File Operations
* **Copy (F5)** — With sidebar-aware destination dialog
* **Move (F6)**
* **Delete (Del, F8)** — `Shift+Del` for instant delete
* **Rename (F2)** — Inline edit, name-only selection
* **New Folder (F7)**
* **New File** — Toolbar or context menu
* **Cut / Copy / Paste** — Full clipboard support
* **Open With** — MIME-based + recent apps
* **Viewer (F3)** — Built-in read-only viewer
* **Editor (F4)** — Built-in text editor
* **Compare (Ctrl+D)** — File A / B / Diff tabs
* **Quick Preview (F11)** — Slide-in panel
* **Open Terminal (F9)**
* **Drag & Drop** — Smart behavior with visual feedback
  - Default: Move  
  - Ctrl: Copy  
  - Shift: Duplicate  
  - Right Drag: Context menu  
* **Properties** — File info + permissions
* **Archive** — zip, tar.gz, tar.bz2, tar.xz
* **Extract** — Auto-extract on double-click

### Custom Toolbar Buttons
* 3 customizable buttons
* Right-click to set name, command, icon
* App picker (supports system, Snap, Flatpak)
* `%f` placeholder for selected file
* Change default editor/terminal

### System
* **Window State Save/Restore**
* **Favorites Persistence**
* **Real-time File Monitoring (Linux, inotify)**
* **Executable Detection** (ELF + shebang)
* **44 Languages UI**

---

## 📌 Highlights

| | |
|---|---|
| ◫ Dual Pane | Toggle and restore last paths |
| 🖼 Thumbnails | Image & video previews |
| 🔍 Fast Search | Recursive, always visible |
| ⌨ IME Support | Stable Korean input |
| 📁 Per-Folder View | Remembers settings |
| ✂ Clipboard Ops | Full file operations |
| 🖱 Mouse Navigation | Back/forward buttons |
| 💾 Window Memory | Auto restore |
| 🌐 Multi-language | 44 languages |
| 🗜 Archive | Compress & extract |
| 💿 Devices | Mount & manage drives |
| ⚡ Fast | Faster than Nautilus |
| 🔧 Custom Buttons | User-defined actions |

---

## 🎮 Shortcuts

| Key | Action |
|---|---|
| F2 | Rename |
| F3 | Viewer |
| F4 | Editor |
| F5 | Copy |
| F6 | Move |
| F7 | New Folder |
| F8 | Delete |
| F9 | Terminal |
| F10 | Sort list columns, refresh list |
| F11 | Preview |
| Del | Delete |
| Shift+Del | Permanent Delete |
| Backspace | Parent folder |
| Enter | Open |
| Ctrl+L | Path input |
| Ctrl+H | Toggle hidden |
| Ctrl+F | Focus search |
| Ctrl+R | Refresh |
| Ctrl+D | Compare |
| Ctrl+X/C/V | Cut/Copy/Paste |
| Ctrl+1~4 | View modes |
| Ctrl+Wheel | Cycle view |
| Alt+Wheel | Font size |
| Alt+1~9 | Bookmarks |
| Mouse 4/5 | Back/Forward |
| Esc | Clear search |

---

## 🖧 Thumbnail Setup

For video thumbnails, install `ffmpegthumbnailer`:

```bash
# Linux
sudo apt install ffmpegthumbnailer
```
---

## 🖥 Supported Platforms

* Windows 10 / 11 (MinGW or MSVC, Qt 6.4+)
* Ubuntu 22.04 / 24.04 or later (GNOME Wayland / X11, Qt 6.4+)

---

## 👤 Author

IYAGI INC
Email: [iyagicom@gmail.com](mailto:iyagicom@gmail.com)
GitHub: https://github.com/iyagicom

---

## 📜 License
Copyright (c) 2026 IYAGI INC. All rights reserved.

This software is provided as executable files only. Source code is not publicly available.

Linux version:
You may use, install, package, and redistribute this software freely for any purpose, including personal, commercial, educational, governmental, and organizational use.

Windows version:
Distributed through the Microsoft Store. Usage and licensing are managed through the MS Store.

