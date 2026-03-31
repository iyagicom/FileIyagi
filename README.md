# FileIyagi v1.4.0

![FileIyagi](fileiyagi.png)


⚡ A **fast and responsive file manager** designed for reliable text input during file renaming and searching.

Enjoy high-speed browsing, keyboard-focused navigation, and smooth thumbnail previews.
The interface automatically adapts to the system language for a seamless user experience.

---

## ✨ Features

### Navigation
* **Breadcrumb path bar** — clickable path segments for quick parent folder navigation
* **Direct path input** — toggle edit mode with `Ctrl+L`, supports `~` for home directory
* **Copy path** — click the current folder segment to copy the full path to clipboard
* **Back / Forward** — mouse buttons 4 & 5, or toolbar ←→ buttons with full history stack
* **Favorites sidebar** — standard folders + user bookmarks
* **Device section** — auto-detected drives and USB volumes with volume labels (Windows & Linux)
* **Auto mount detection** (Linux) — sidebar refreshes when USB is plugged or unplugged
* **My Disk** — click "My Disk" in the sidebar to see all drives including unmounted ones; click to mount instantly
* **Recent files** — per-folder recent file list at the bottom of the sidebar, auto-updated on navigation
* **Recent paths history** — last 15 visited paths saved in the path-bar dropdown; persists across app restarts

### Dual Pane (2-Panel Mode)
* **Dual pane toggle** — ◫ button at the far right of the status bar; left = current panel, right = starts at home (~/)
* **Last path remembered** — each pane restores its last visited path across sessions
* **Session persistence** — dual pane ON/OFF state is preserved between app restarts

### View Modes
* **Details view** — name, size, ext, date columns with directory-first sorting; click column headers to sort
* **Icon view** — three sizes: small (96px), medium (150px), large (224px)
* **Thumbnails** — auto-generated for images (Qt) and videos (`ffmpegthumbnailer`), XDG/platform cache
* **Per-folder view mode** — each folder remembers its last view mode
* **Hidden file toggle** — `Ctrl+H` or the "." button
* **Font size** — adjust live with `Alt+Wheel` (7–24pt)
* **View mode cycling** — `Ctrl+Wheel` or `Ctrl+1–4`
* **Sort buttons** — status bar buttons for quick sort by name / size / ext / date
* **Fixed column widths** — size, date, and ext columns are fixed width; only the name column fills the remaining space (columns are not user-resizable)

### Search
* **Always-visible search bar** — active at all times on the right side of the toolbar
* **Recursive search** — searches all subdirectories under the current folder
* **300 ms debounce** — starts after a short pause in typing
* **Search-preserving file open** — opening a file from results keeps the search active
* **Drag from search results** — drag files to other apps directly from search results
* **Search result column layout** — name and location columns fill equally (50/50), size / ext / date are fixed width

### File Operations
* **Copy (F5)** — destination picker with Favorites & Devices sidebar; pending items can be removed from the queue with the X button; the currently copying item hides the X button automatically
* **Move (F6)** — destination picker with Favorites & Devices sidebar
* **Delete (Del, F8)** — with confirmation dialog; `Shift+Del` skips confirmation
* **Rename (F2)** — inline editing, name pre-selected without extension
* **New folder (F7)** — works from anywhere, including sidebar focus
* **New file** — create an empty file in the current folder (toolbar button or right-click menu); preferred editor configurable via right-click on the toolbar button
* **Cut (Ctrl+X)** — cut files with semi-transparent visual indicator; paste moves them
* **Copy to clipboard (Ctrl+C)** — copy file(s) to clipboard for paste in other apps
* **Paste (Ctrl+V)** — paste files; cut files are moved, copied files are duplicated; works from anywhere in the window (sidebar, toolbar, etc.) without requiring a click on the file list first
* **Open With** — MIME-based app list with recommended apps; remembers last used app per file type
* **Open Terminal (F9)** — open a terminal in the current folder; preferred terminal emulator configurable via right-click on the toolbar button
* **File Viewer (F3)** — built-in read-only viewer for text and images; supports maximize button
* **File Editor (F4)** — built-in text editor; F4 with no selection creates a new file; supports maximize button; drag-to-select auto-scroll speed is capped for comfortable use
* **Compare Files (Ctrl+D)** — pick two files and view a 3-tab diff (File A / File B / Diff with color)
* **Quick Preview (F11)** — slide-in preview panel showing image or text of selected file
* **Drag & drop** — drag files to other apps (image viewers, GIMP, etc.); drag ghost matches column width
* **Drag & drop rules** — default drag = Move (regardless of drive); Ctrl+drag = Copy; Shift+drag = Duplicate (auto-incremented name: `file (1).txt`); right-click drag = context menu (Move / Copy / Cancel); cursor feedback during drag (Move arrow / Copy ➕ / forbidden 🚫); status bar shows real-time "Moving: file.txt → folder" message
* **Properties** — name, path, size, modification date; folder shows direct + total recursive file count; permission (chmod) change
* **Compress** — zip / tar.gz / tar.bz2 / tar.xz formats
* **Extract** — double-click archive to extract into a named folder and navigate into it

### Toolbar Custom Buttons
* **3 configurable custom buttons** — in the title bar, next to the terminal button
* **Right-click to configure** — set a name, command, and icon for each button; icon is auto-loaded from the selected app's `.desktop` entry
* **App chooser dialog** — searchable list of all installed apps (standard paths + Snap + Flatpak); `%f` in the command is replaced with the selected file path at runtime; if `%f` is omitted the current folder is appended automatically
* **New File / Terminal app override** — right-click either button to pick a different app from the same chooser dialog; the preference is saved and used on the next click

### System
* **Window size/position saved** — restored on next launch
* **Bookmark persistence** — saved to OS-appropriate config path (Windows: %APPDATA%, Linux: ~/.config)
* **Real-time file detection** (Linux) — inotify-based, new files appear instantly
* **Executable detection** — ELF magic + shebang check (works correctly on NTFS drives)
* **44-language UI** — auto-translated interface following system locale

### Key Features

|                                     |                                                                          |
| ----------------------------------- | ------------------------------------------------------------------------ |
| ◫ **Dual Pane**                     | Two-panel mode toggled by the ◫ status bar button; last paths restored   |
| 🖼 **Thumbnail Preview**            | Automatic image and video thumbnails using XDG cache                     |
| 🔍 **Fast Search**                  | Recursive subfolder search with always-visible search bar                |
| ⌨ **Full Korean IME Support**       | Native Qt6 input — works correctly in rename and search                  |
| 📁 **Per-Folder View Mode**         | Each folder remembers its last view setting                              |
| ✂ **Cut / Copy / Paste**           | Full clipboard file operations with visual cut indicator                 |
| 🖱 **Mouse Back / Forward Buttons** | Natural history navigation                                               |
| 💾 **Auto Window State Save**       | Window size and position restored on next launch                         |
| 🌐 **44-Language UI**               | UI language follows system locale                                        |
| 🗜 **Archive Compress / Extract**   | Double-click to extract zip / tar.gz / 7z / rar; compress selected files |
| 💿 **My Disk**                      | View and mount all drives directly from the sidebar                      |
| 📂 **Recent Files**                 | Per-folder recent file list in the sidebar                               |
| ⚡ **Fast Loading**                  | Faster startup and browsing than Nautilus                                |
| 🖥 **Default File Manager Support** | xdg-mime integration and file-manager mouse key support                  |
| 🔧 **Custom Toolbar Buttons**       | 3 user-defined buttons with app chooser, `%f` file arg, and saved icon  |
| 🕑 **Persistent Path History**      | Last 15 visited paths saved across restarts                              |
| 🖱 **Smart Drag & Drop**            | Default=Move, Ctrl=Copy, Shift=Duplicate, right-click=context menu      |


## 🎮 Keyboard Shortcuts

| Key | Action |
|---|---|
| F2 | Rename (selects name only, not extension) |
| F3 | File Viewer (read-only, text & image) |
| F4 | File Editor (built-in text editor; no selection = new file) |
| F5 | Copy to folder |
| F6 | Move to folder |
| F7 | New folder |
| F8 | Delete (with confirmation) |
| F9 | Open terminal in current folder |
| F10 | Close app |
| F11 | Toggle quick preview panel |
| Del | Delete (with confirmation) |
| Shift+Del | Delete (no confirmation) |
| Backspace | Go to parent folder |
| Enter | Open / navigate into folder |
| Ctrl+L | Toggle path edit mode |
| Ctrl+H | Toggle hidden files |
| Ctrl+F | Focus search bar |
| Ctrl+R | Refresh |
| Ctrl+D | Compare two files (3-tab: File A / File B / Diff) |
| Ctrl+X | Cut |
| Ctrl+C | Copy to clipboard |
| Ctrl+V | Paste |
| Ctrl+1 | Details view |
| Ctrl+2 | Icon view (small) |
| Ctrl+3 | Icon view (medium) |
| Ctrl+4 | Icon view (large) |
| Ctrl+Wheel | Cycle view modes |
| Alt+Wheel | Adjust font size |
| Alt+1~9 | Jump to bookmark 1–9 |
| Mouse Button 4 | Back |
| Mouse Button 5 | Forward |
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

