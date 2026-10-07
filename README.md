# FileIyagi

**A fast file manager for Windows and Linux — up to four panes side by side, and your servers, phone and drives in one sidebar.**

[English](README.md) · [한국어](README_ko.md)

![FileIyagi](fileiyagi.png)

## Why FileIyagi?

- **Up to four panes side by side.** Copy from one folder to another without juggling windows. Turn on 2, 3 or 4 panes with one click, and every pane remembers where it was.
- **Servers feel like folders.** Connect to SFTP, SMB/Samba, FTP or WebDAV from the sidebar and browse them like local disks. Android phones and cameras (MTP) appear on their own.
- **Find anything as you type.** The search box is always in the title bar. Results come in as you type, grouped by folder, and you can drag files straight out of the results.
- **Look before you open, fix it on the spot.** Quick Preview (F11), built-in file compare (Ctrl+D), a text editor (F4), an image editor that opens when you press F4 on a picture, and thumbnails that stay cached.
- **Keyboard first, like a classic commander.** F7 copy, F6 move, F2 rename, Ctrl+N new folder, Del delete, Ctrl+Z undo, pattern selection, a Basket for gathering files from many folders.
- **Same app on both systems.** Moving between Windows and Linux? Same layout, same shortcuts. On Windows it can even read your Linux EXT4 partitions.

## Features

### Browse
- **Clickable path bar** — click a segment to go there, click the current folder to copy its path. `F12` switches to typing a path (`~` supported)
- **Copy a file's path** — select one file and its name appears at the end of the path bar; click it to copy the full path
- **Back, forward, up** — toolbar buttons and mouse buttons 4 and 5
- **Favorites sidebar** — Home, Desktop, Documents and your own bookmarks; jump with `Alt+1~9`
- **Devices** — drives and USB volumes appear as you plug them in. "My Devices" also lists unmounted disks and mounts them with one click
- **Recent files per folder**, and a **recent-paths list** that survives restarts
- **Type to jump** to a file by name

### Views — all remembered per folder
- **Details** (`Ctrl+1`) · **List** (`Ctrl+2`) · **Icons small/medium/large** (`Ctrl+3~5`)
- **Thumbnails** — images, videos and the first page of PDFs, generated automatically and served from cache afterwards
- **Sorting** — name, size, extension, date (`Ctrl+6~9`, status-bar buttons, or column headers)
- **Subfolder grid** (`Ctrl+Tab`) — folders gathered in a grid on top, files only in the list below
- **View mode, sort order and the subfolder grid belong to the folder.** Each folder keeps its own, and it opens the way you left it even after a restart
- Hidden-file toggle (`Ctrl+H`), live font size (`Alt+Wheel`), columns that widen with the font

### Multi-pane
- **2, 3 or 4 panes** — `F1` or the ◫ button in the status bar. Splitter ratios and each pane's path are remembered separately for each pane count
- **Enlarge active pane** — optional, gives the pane you're working in more room
- **Three window sizes** to cycle through (`Ctrl+S`); window size and position remembered

### Search
- **Search box in the title bar** — always there; stop typing and it searches every subfolder
- **Results grouped by folder** — click a folder row to go there. Icon and thumbnail views work in results too
- **Work straight from the results** — open, copy, move, delete, preview, drag out, compress and extract
- Opening a file keeps the search active

### File operations
- **Copy** (`F7`) · **Move** (`F6`) — destination picker with favorites and devices; pending items can be removed from the queue
- **Drag and drop** — move by default, `Alt` to copy, `Shift` to duplicate (auto-named), right-drag for a Move/Copy/Shortcut menu
- **Rename** (`F2`) — starts with just the name selected, not the extension
- **Batch rename** (`F8`) — prefix, suffix, find and replace, numbering
- **New folder** (`Ctrl+N`), **new folder from selection**, new file from template
- **Select by pattern** (`Ctrl+Shift+S`) — wildcards like `*.jpg`
- **Undo** (`Ctrl+Z`) — create, delete, copy, move and batch rename, several steps back
- **Delete** (`Del`) goes to the trash; `Shift+Del` deletes permanently — and even that can be undone for a few days
- **Basket** (`Alt+B`) — gather files while moving between folders, then compress, copy, move or delete them in one go
- **Sync and back up two folders** (`F10`) — one-way backup or two-way sync, with a preview of what will change
- **Open With** that remembers your choice per file type
- **Properties** — size, path, dates, file counts for folders, permissions
- **File tags and stars**, **folder notes**

### Archives
- **Compress** — zip · tar.gz · tar.bz2 · tar.xz · 7z
- **Files from several folders into one archive** — keep the Compress window open, go to another folder (or another pane), select files and click "Add Selection", or drag them into the window. Files picked in search results work too
- **Extract** — double-click an archive to extract it into a folder of the same name, or right-click "Extract Here"

### View and edit
- **Quick preview** (`F11`) — images, text and music in a side panel as you select. For music, the folder's songs become a playlist and unchecked songs are skipped
- **Viewer** (`F3`) — text, images, PDF, music, video and Excel (.xlsx) without a separate program
- **Text editor** (`F4`) — with nothing selected it creates a new file
- **Image editor** (`F4` on a picture) — crop, rotate, flip, straighten, resize, color, effects, text, and **fit to a target file size**. The original changes only when you press Save
- **Excel viewer/editor** — open and edit .xlsx without Excel
- **File compare** (`Ctrl+D`) — two files and their differences side by side
- **Terminal** (`F9`) — opens in the current folder

### Remote and devices
- **SFTP · SMB/Samba · FTP · WebDAV** — "Connect to Server…" in the sidebar, then browse like a local disk
- **Android (MTP), cameras and network mounts** listed automatically
- **Send and receive files over the network**
- **Windows: read Linux EXT4 partitions** — same views, sorting, copy and drag and drop
- **Windows: recover permanently deleted files**

### Part of the system
- **Set as the default file manager** — one button from the title-bar icon
- **Replaces other apps' Open/Save dialogs** — attach or save a file from your browser and FileIyagi opens. When attaching, you can collect files from several folders and add them at once; when saving, clicking a file suggests the next numbered name
- **Three toolbar buttons** you can point at any app or command, with `%f` for the selected file
- **12 UI languages**, and it uses whatever input method you've set as default

### Linux helpers (Settings → Convenience)
- **Hibernate setup** — finds out why suspend or hibernate fails and fixes it in one go
- **Log analysis** — explains why the PC crashed as causes and fixes, not raw logs
- **Journal flood guard** — stops one program from filling the disk with logs
- **Extract audio from video** — pull the audio track out without re-encoding, and put it back
- **System information** — hardware and drivers, including the IDs you need to look up a driver. All of it can be copied

## Shortcuts

| Key | Action | Key | Action |
|---|---|---|---|
| `F1` | Toggle dual pane | `Ctrl+N` | New folder |
| `F2` | Rename | `Ctrl+Z` | Undo |
| `F3` | Viewer | `Ctrl+C` `X` `V` | Copy, cut, paste |
| `F4` | Editor (image editor on pictures) | `Ctrl+F` | Focus search |
| `F5` | Refresh | `Ctrl+D` | Compare files |
| `F6` | Move | `Ctrl+H` | Hidden files |
| `F7` | Copy | `Ctrl+Tab` | Subfolder grid |
| `F8` | Batch rename | `Ctrl+1~5` | View mode |
| `F9` | Terminal | `Ctrl+6~9` | Sort |
| `F10` | Sync and backup | `Ctrl+Shift+S` | Select by pattern |
| `F11` | Quick preview | `Alt+B` | Add to Basket |
| `F12` | Type a path | `Del` / `Shift+Del` | Delete / delete permanently |

The full list is in the app under `Ctrl+F1`.

## Download

**[⬇ Latest release](https://github.com/iyagicom/FileIyagi/releases/latest)**

| Your system | File to pick |
|---|---|
| Windows 10 / 11 | [Microsoft Store](https://apps.microsoft.com/search?query=FileIyagi) |
| Ubuntu 24.04 · Debian | `.deb` marked **ubuntu24.04** |
| Ubuntu 26.04 | `.deb` marked **ubuntu26.04** |
| Fedora · openSUSE | `.rpm` |
| Arch · Manjaro | `.pkg.tar.zst` |
| Any other Linux | `.AppImage` (run without installing) or `.zip` |

```bash
sudo apt install ./fileiyagi_*_amd64.deb     # Ubuntu / Debian
sudo dnf install ./fileiyagi-*.rpm           # Fedora
sudo pacman -U fileiyagi-*.pkg.tar.zst       # Arch
```

Everything the app needs is bundled — nothing else to install.

## License

[License](LICENSE) · [Privacy policy](privacy-policy.md)
