# FileIyagi v1.47.10

![FileIyagi](fileiyagi.png)


⚡ A **fast and responsive file manager** designed for reliable text input during file renaming and searching.

Enjoy high-speed browsing, keyboard-focused navigation, and smooth thumbnail previews.
The interface automatically adapts to the system language for a seamless user experience.

---

## ✨ Features

### Navigation
* **Breadcrumb path bar** — clickable path segments for quick parent folder navigation; click empty area to enter path edit mode
* **Single-click folder open** — ① toolbar toggle button; when enabled, single-clicking a folder navigates into it
* **Direct path input** — toggle edit mode with `Ctrl+L`, supports `~` for home directory
* **Copy path** — click the current folder segment to copy the full path to clipboard
* **File path crumb** — when a single file is selected, its name appears as a teal segment at the end of the path bar (up to 8 characters; full path in tooltip); click to copy the complete file path to clipboard; disappears on navigation or deselection
* **Back / Forward** — mouse buttons 4 & 5, or toolbar ←→ buttons with full history stack
* **Favorites sidebar** — standard folders + user bookmarks
* **Device section** — auto-detected drives and USB volumes with volume labels (Windows & Linux)
* **Auto mount detection** (Linux) — sidebar refreshes when USB is plugged or unplugged
* **My Disk** — click "My Disk" in the sidebar to see all drives including unmounted ones; click to mount instantly
* **Connect to Server** (Linux) — click "+ Connect to Server..." in the sidebar to mount SFTP, SMB/Samba, FTP, WebDAV, iPhone (AFC), or Bluetooth OBEX via GVFS; connection history saved for quick reconnect; right-click connected item to disconnect
* **Android / Camera / Network mounts in sidebar** — all GVFS-mounted devices (MTP, gphoto2, SFTP, SMB, etc.) appear automatically in the sidebar after connection
* **Recent files** — per-folder recent file list at the bottom of the sidebar, auto-updated on navigation
* **Recent paths history** — last 15 visited paths saved in the path-bar dropdown; persists across app restarts

### Dual Pane (2-Panel Mode)
* **Dual pane toggle** — ◫ button at the far right of the status bar; left = current panel, right = starts at home (~/)
* **Last path remembered** — each pane restores its last visited path across sessions
* **Session persistence** — dual pane ON/OFF state is preserved between app restarts

### View Modes
* **Details view (Ctrl+1)** — name, size, ext, date columns with directory-first sorting; click column headers to sort
* **List view (Ctrl+2)** — compact single-column list with small icons and names
* **Icon view** — three sizes: small (Ctrl+3, 96px), medium (Ctrl+4, 150px), large (Ctrl+5, 224px)
* **Thumbnails** — auto-generated for images (Qt) and videos (`ffmpegthumbnailer`), XDG/platform cache; disk-cached thumbnails load instantly even during scroll or navigation
* **Per-folder view mode** — each folder remembers its last view mode
* **Subfolder panel (F-35)** — grid of subfolders in the current directory for quick navigation; toggle with the ⊞ status bar button or `Ctrl+Tab`
* **Hidden file toggle** — `Ctrl+H` or the "." button
* **Font size** — adjust live with `Alt+Wheel` (7–24pt)
* **View mode cycling** — `Ctrl+Wheel` or `Ctrl+1–5`
* **Sort buttons** — status bar buttons for quick sort by name / size / ext / date
* **Font-proportional column widths** — the size, date, and ext columns scale with the current font size (optimized around 11 pt); increasing the font widens the columns so text is never clipped, decreasing it narrows them. The name column fills the remaining space
* **EXT4 partition browser (Windows)** — a Linux user working on Windows can open and read files from their EXT4 (Linux) partitions; requires administrator mode. Read-only. The EXT4 view behaves like a normal folder view — all view modes (Ctrl+1–5) render identically, and sorting by name / size / date (Ctrl+6–8) works with folders listed first

### Search
* **Always-visible search bar** — active at all times on the right side of the toolbar
* **Recursive search** — searches all subdirectories; results are grouped by folder in a tree view (click a folder node to navigate there); recent / starred / trash views retain the flat list
* **300 ms debounce** — starts after a short pause in typing
* **Search-preserving file open** — opening a file from results keeps the search active
* **Drag from search results** — drag files to other apps directly from search results
* **Search result column layout** — name / size / ext / date columns; folder nodes are shown as non-selectable group headers (location column replaced by tree structure)

### File Operations
* **Copy (F5)** — destination picker with Favorites & Devices sidebar; pending items can be removed from the queue with the X button; the currently copying item hides the X button automatically
* **Move (F6)** — destination picker with Favorites & Devices sidebar
* **Delete (Del, F8)** — with confirmation dialog; `Shift+Del` skips confirmation
* **Rename (F2)** — inline editing, name pre-selected without extension
* **New folder (F7)** — works from anywhere, including sidebar focus
* **Select by Pattern (Ctrl+Shift+S)** — wildcard file selection in the current folder; patterns without `*` or `?` automatically become `*pattern*` contains search; also available in the right-click menu
* **New Folder from Selection** — select 2+ files, right-click → "New Folder from Selection"; enter a folder name and the selected files are moved into it; supports Ctrl+Z undo
* **New File from Template** (Linux) — right-click in empty space → "New File from Template" submenu lists files from `~/Templates/`; duplicate names are auto-numbered (`filename (1).ext`); supports Ctrl+Z undo
* **Cut (Ctrl+X)** — cut files with semi-transparent visual indicator; paste moves them
* **Copy to clipboard (Ctrl+C)** — copy file(s) to clipboard for paste in other apps
* **Paste (Ctrl+V)** — paste files; cut files are moved, copied files are duplicated; works from anywhere in the window (sidebar, toolbar, etc.) without requiring a click on the file list first
* **Open With** — MIME-based app list with recommended apps; remembers last used app per file type
* **Open Terminal (F9)** — open a terminal in the current folder; preferred terminal emulator configurable via right-click on the toolbar button
* **Open in New Window** — right-click a folder → "Open in New Window" launches a new FileIyagi instance at that path
* **Open as Administrator** (Linux) — right-click a folder → "Open as Administrator" relaunches with `pkexec` for elevated access; only shown when `pkexec` is available
* **Burn to Disc** (Linux) — right-click selected files → "Burn to Disc..." opens brasero or k3b; shown only when a disc burning app is installed
* **Autorun detection** (Linux) — when a USB or disk is mounted, automatically checks for `autorun.sh` and offers to run it
* **Scripts submenu** (Linux) — right-click → "Scripts" submenu lists executable files from `~/.local/share/nautilus/scripts/`; selected file paths are passed via Nautilus-compatible environment variables
* **File Viewer (F3)** — built-in read-only viewer for text and images; supports maximize button
* **File Editor (F4)** — built-in text editor; F4 with no selection creates a new file; supports maximize button; drag-to-select auto-scroll speed is capped for comfortable use
* **Compare Files (Ctrl+D)** — pick two files and view a 3-tab diff (File A / File B / Diff with color)
* **Quick Preview (F11)** — slide-in preview panel showing image or text of selected file
* **Drag to select** — drag over files to select them, just like on Android; unlike most file managers, dragging does not accidentally move files
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
* **12-language UI** — English, Korean, Japanese, Chinese, German, Spanish, French, Portuguese, Russian, Turkish, Vietnamese, Indonesian; follows the system locale automatically
* **Set as default file manager** — click the app icon in the title bar; the popup includes a "Set as Default" button that registers FileIyagi via `xdg-mime` and `gsettings` in one click; button turns green and disables itself when already set
* **System-wide File Open / Save dialog (Windows)** — once the file-dialog picker is registered, **every** application's file Open **and** Save dialog opens FileIyagi instead of the standard Windows dialog — Chrome, Edge, PDFIyagi, and most Win32 / Electron / Qt apps. Registered per-user (HKCU), no admin rights needed. This is a separate toggle from Explorer right-click integration, so it can be turned off on its own
* **Smart system-dialog fallback (Windows)** — sandboxed / packaged apps (Notepad, Media Player, and other UWP / WinUI apps) and legacy apps that cannot handle a custom dialog (e.g. Illustrator CC2015) automatically get the genuine Windows dialog instead — forwarded straight to `comdlg32.dll`, fully transparent to the app. The exclusion list is user-extensible via the registry: `HKCU\Software\IYAGI-INC\FileIyagi\pickerExcludedApps` (REG_SZ, `;`-separated exe names)

### Key Features

|                                     |                                                                          |
| ----------------------------------- | ------------------------------------------------------------------------ |
| ◫ **Dual Pane**                     | Two-panel mode toggled by the ◫ status bar button; last paths restored   |
| 📂 **Subfolder Panel**              | Grid of subfolders for instant navigation (F-35)                         |
| 🖼 **Thumbnail Preview**            | Automatic image and video thumbnails using XDG cache                     |
| 🔍 **Fast Search**                  | Recursive subfolder search; results grouped by folder in a tree view     |
| ⌨ **Full Korean IME Support**       | Native Qt6 input — works correctly in rename and search                  |
| 📁 **Per-Folder View Mode**         | Each folder remembers its last view setting                              |
| ✂ **Cut / Copy / Paste**           | Full clipboard file operations with visual cut indicator                 |
| 🖱 **Mouse Back / Forward Buttons** | Natural history navigation                                               |
| 💾 **Auto Window State Save**       | Window size and position restored on next launch                         |
| 🌐 **12-Language UI**               | UI language follows system locale                                        |
| 🗜 **Archive Compress / Extract**   | Double-click to extract zip / tar.gz / 7z / rar; compress selected files |
| 💿 **My Disk**                      | View and mount all drives directly from the sidebar                      |
| 🌐 **Connect to Server**            | Mount SFTP / SMB / FTP / WebDAV / iPhone / Bluetooth via GVFS; history saved |
| 🔒 **Open as Administrator**        | Relaunch with pkexec for elevated folder access (Linux)                  |
| 🪟 **Open in New Window**           | Right-click folder to open it in a new FileIyagi instance                |
| 📀 **Burn to Disc**                 | Right-click files → launch brasero/k3b if installed (Linux)             |
| 📂 **Recent Files**                 | Per-folder recent file list in the sidebar                               |
| ⚡ **Fast Loading**                  | Faster startup and browsing than Nautilus                                |
| 🖥 **Default File Manager** | One-click setup via title bar icon; `xdg-mime` + `gsettings` registered automatically |
| 🌐 **File Picker (Linux)**  | XDG Portal FileChooser backend — every app's Open/Save dialog opens inside FileIyagi |
| 🪟 **File Open/Save Dialog (Windows)** | COM CLSID intercept — **every** app's Open **and** Save dialog opens inside FileIyagi |
| 🐧 **EXT4 Partition Browser (Windows)** | Read Linux EXT4 partitions from Windows (admin mode); full view modes + sorting like a normal folder |
| 🔢 **Auto-increment Save Name (v1.46.0)** | Click a file in the Save dialog to auto-suggest the next name — e.g. click `276-21 주1동.pdf` → suggests `276-21 주2동.pdf` |
| 🔧 **Custom Toolbar Buttons**       | 3 user-defined buttons with app chooser, `%f` file arg, and saved icon  |
| 🕑 **Persistent Path History**      | Last 15 visited paths saved across restarts                              |
| 🖱 **Smart Drag & Drop**            | Default=Move, Ctrl=Copy, Shift=Duplicate, right-click=context menu      |
| ① **Single-Click Folder Open**      | Toolbar toggle; single-click navigates into folders                      |
| 🎯 **Select by Pattern**            | Wildcard file selection in current folder (`Ctrl+Shift+S`)               |
| 📍 **File Path Crumb**              | Selected file's full path shown and copyable in the path bar             |


## 🎮 Keyboard Shortcuts

| Key | Action |
|---|---|
| F1 | Toggle dual pane |
| Ctrl+F1 | Keyboard shortcuts (this window) |
| F2 | Rename (selects name only, not extension) |
| F3 | File Viewer (read-only, text & image) |
| F4 | File Editor (built-in text editor; no selection = new file) |
| F5 | Refresh + auto column width |
| F6 | Move to folder |
| F7 | Copy to folder |
| F8 | Sync + Backup (dual pane only) |
| F9 | Open terminal in current folder |
| F10 | Batch rename |
| F11 | Toggle quick preview panel |
| F12 | Toggle path bar (buttons ↔ text input) |
| Del | Delete |
| Shift+Del | Delete (no confirmation) |
| Backspace / Alt+↑ | Go to parent folder |
| Alt+← | Go back |
| Alt+→ | Go forward |
| Drag over files | Select files like on Android — no accidental move |
| Enter | Open / navigate into folder |
| Ctrl+S | Cycle window size (3 steps: compact / medium / large) |
| Ctrl+Tab | Toggle subfolder panel (⊞) |
| Ctrl+H | Toggle hidden files |
| Ctrl+F | Focus search bar |
| Ctrl+N | New folder |
| Ctrl+Z | Undo last file operation |
| Ctrl+R | Refresh |
| Ctrl+D | Compare two files (3-tab: File A / File B / Diff) |
| Ctrl+X | Cut |
| Ctrl+C | Copy to clipboard |
| Ctrl+V | Paste |
| Ctrl+Shift+S | Select files by pattern |
| Ctrl+Shift+T | Show trash |
| Ctrl+1 | Details view |
| Ctrl+2 | List view (names only) |
| Ctrl+3 | Icon view (small, 96px) |
| Ctrl+4 | Icon view (medium, 150px) |
| Ctrl+5 | Icon view (large, 224px) |
| Ctrl+6 | Sort by name |
| Ctrl+7 | Sort by size |
| Ctrl+8 | Sort by date |
| Ctrl+9 | Sort by extension |
| Ctrl+0 | Auto-fit column widths |
| Ctrl+Wheel | Cycle view modes |
| Ctrl+↑ | Font size +1 |
| Ctrl+↓ | Font size -1 |
| Alt+Wheel | Adjust font size |
| Alt+drag | Create symbolic link |
| Alt+1~9 | Jump to bookmark 1–9 |
| Mouse Button 4 | Back |
| Mouse Button 5 | Forward |
| Esc | Clear search |

---

## 🚀 Installation

### Linux — zip (all distros)

1. Download `FileIyagi-vX.X.X-linux-x64.zip` and extract it
2. Run:
   ```bash
   bash install.sh
   ```
   Installs the binary to `~/.local/bin/`, registers the icon and `.desktop` file, sets FileIyagi as the default file manager, and configures the XDG Portal FileChooser backend for browser Save-As dialogs.

**Qt6 required** — install if missing:

| Distro | Command |
|--------|---------|
| Ubuntu / Debian | `sudo apt install libqt6core6 libqt6widgets6 libqt6sql6 libqt6dbus6` |
| Fedora | `sudo dnf install qt6-qtbase qt6-qtsql` |
| Arch Linux | `sudo pacman -S qt6-base` |
| openSUSE | `sudo zypper install libqt6-qtbase` |

### Linux — deb (Ubuntu / Debian)

```bash
sudo dpkg -i fileiyagi_X.X.X_amd64.deb
```

### Windows

Available on the [Microsoft Store](https://apps.microsoft.com/search?query=FileIyagi).

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

## 📋 Changelog

### v1.47.11 (2026-07-05)
- **Complete 12-language UI** — all 682 UI strings professionally re-translated for 10 languages (German, Spanish, French, Indonesian, Portuguese, Russian, Turkish, Vietnamese + new: **Japanese, Chinese**); Korean also completed (311 previously missing strings, including the entire Settings dialog). New `tools/gpt_translate.py` export/import pipeline with placeholder validation replaces raw machine translation
- **Font size range widened** — Ctrl+↑/↓ / Alt+Wheel / Settings slider now allow the full documented 7–24 pt range (previously capped at base ±5, which silently stopped at 16 pt)

### v1.47.10 (2026-07-04)
- **Qt apps (QGIS, etc.) now receive picked files correctly** — the picker COM dialog now honors the `IFileDialogEvents::OnFileOk` contract. Qt's native dialog helper only accepts a result if it can read it during the `OnFileOk` event; without it, every Qt app silently treated a successful pick as *Cancel*. The event sink registered via `Advise()` is now stored and `OnSelectionChange` + `OnFileOk` are fired on success
- **Sandboxed / packaged apps fall back to the system dialog** — UWP / WinUI file pickers run inside an AppContainer broker process that cannot launch the full-trust FileIyagi picker (Notepad showed an empty result, Media Player crashed). AppContainer / packaged processes are now detected (`TokenIsAppContainer` + `GetCurrentPackageFullName`) and forwarded to the genuine `comdlg32.dll` implementation
- **App exclusion list** — apps that cannot handle a custom dialog get the genuine system dialog; extensible via `HKCU\Software\IYAGI-INC\FileIyagi\pickerExcludedApps` (REG_SZ, `;`-separated)
- **Picker debug log** — `%TEMP%\picker_debug.log` now appends with a timestamp and the host process name per invocation (previously overwritten each time), so failures can be correlated with the calling app

### v1.47.0 (2026-07-04)
- **System-wide file dialog (Windows)** — the FileIyagiPicker COM component now intercepts **every** application (not just browsers), so any app's file Open dialog opens FileIyagi. Added **Save dialog** support (`CLSID_FileSaveDialog`) — Save-As dialogs also open FileIyagi. FileIyagi's own picker process is the only one excluded (recursion guard)
- **Font-proportional column widths** — Details / search / recent / starred / EXT4 column widths now scale with the font size instead of being fixed at 11 pt, so larger fonts no longer clip text
- **EXT4 partition view parity (Windows)** — the read-only EXT4 Linux-partition browser now behaves like a normal folder view: icon / list modes (Ctrl+1–5) use the same thumbnail delegate and rendering, and sorting by name / size / date (Ctrl+6–8) works correctly (numeric size, chronological date, folders first)
- **EXT4 breadcrumb path bar (Windows)** — the EXT4 view's path bar is now a clickable breadcrumb (like a normal folder) instead of a plain text field; click any segment to jump to that parent folder, including a leading `/` for the partition root

### v1.46.3 (2026-06-17)
- **Save dialog auto-increment** — clicking a file in the Save dialog auto-suggests the next name (`abc.pdf` → `abc2.pdf`, `abc9.pdf` → `abc10.pdf`); extension is preserved automatically
- **Save dialog extension preserve** — typing a name without extension keeps the original file's extension; typing `.xxx` overrides it
- **Save dialog default filename** — calling apps (Chrome, PdfIyagi) now pass their suggested filename; picker stays on top of the calling window (no more falling behind Chrome)
- **Alt+1~9 bookmark jump** — press Alt and a number to jump directly to bookmark 1~9; sidebar shows number hints while Alt is held
- **PDF viewer (Windows)** — built-in PDF viewer using Qt6 `QPdfDocument`; page navigation and zoom support
- **File viewer themes** — Monokai and Dark themes for the built-in text viewer/editor (F3/F4)
- **Drag to select** — drag over files to select them like on Android; unlike other file managers, dragging does not move files accidentally

### v1.45.8 (2026-06-14)
- **Bug fix** — Font size and row height slider changes not reflected in file view
  - Widgets with QSS stylesheets require explicit `font-size` in stylesheet (not just `setFont()`)
  - `ThumbnailDelegate::sizeHint()` now returns row height directly (removed `setUniformRowHeights` toggle)
- **Bug fix** — Dual-pane right panel not syncing row height and font changes
  - Added `rowHeightChanged` / `fontSizeChanged` signal chain for both panels

### v1.45.0 (2026-05)
- **Row height slider** — Adjust file list row height in real time via Ctrl+F1 settings
- **Font size slider** — Adjust file list font size in real time via Ctrl+F1 (sidebar and path bar keep system font)
- **Multi-column list view** — Ctrl+2 list view adapts columns to window width
- Icon view grid size dynamically adjusts to row height setting

### v1.44.0 (2026-05)
- **Folder memo** — Write and save notes per folder (preview banner at panel top, click to edit)

### v1.43.0 (2026-04)
- **Tag system** — Tag files and browse by tag
- Tag section in sidebar (`tag://` paths)
- Tagged files highlighted in green in the file view

### v1.42.0 (2026-03)
- **Windows COM file picker** — Replace browser (Chrome/Edge) file-open dialog with FileIyagi (FileIyagiPicker.dll)

### v1.40.0 (2026-03)
- **Search tree view** — Search results displayed as folder-grouped tree
- Multi-instance support, new window, folder icon theming, font system unification

---

## 👤 Author

IYAGI-INC
Email: [iyagicom@gmail.com](mailto:iyagicom@gmail.com)
GitHub: https://github.com/iyagicom

---

## 📜 License
Copyright (c) 2026 IYAGI-INC. All rights reserved.

This software is provided as executable files only. Source code is not publicly available.

Linux version:
You may use, install, package, and redistribute this software freely for any purpose, including personal, commercial, educational, governmental, and organizational use.

Windows version:
Distributed through the Microsoft Store. Usage and licensing are managed through the MS Store.

