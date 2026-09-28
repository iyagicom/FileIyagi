# FileIyagi

**A fast file manager for Windows and Linux — up to four panes side by side, and your servers, phone and drives in one sidebar.**

[English](README.md) · [한국어](README_ko.md)

![FileIyagi](fileiyagi.png)

## Why FileIyagi?

- **Up to four panes side by side.** Copy from one folder to another without juggling windows. Turn on 2, 3 or 4 panes with one click, and every pane remembers where it was.
- **Servers feel like folders.** Connect to SFTP, SMB/Samba, FTP or WebDAV from the sidebar and browse them like local disks. Android phones and cameras (MTP) appear on their own.
- **Find anything as you type.** The search box is always in the title bar. Results come in as you type, grouped by folder, and you can drag files straight out of the results.
- **Look before you open.** Quick Preview (F11), built-in file compare (Ctrl+D), a text editor (F4), and thumbnails that stay cached.
- **Keyboard first, like a classic commander.** F5 copy, F6 move, F7 new folder, F8 delete, F2 rename, pattern selection, a Basket for gathering files from many folders.
- **Same app on both systems.** Moving between Windows and Linux? Same layout, same shortcuts. On Windows it can even read your Linux EXT4 partitions.

## Features

### Browse
- Clickable breadcrumb path bar, direct path input (`Ctrl+L`), back/forward with mouse buttons
- Favorites, drives and USB volumes in the sidebar; unmounted disks mount with one click
- Details, list and three icon sizes; each folder remembers its view
- Subfolder grid, hidden-file toggle, live font size (`Alt+Wheel`)

### Multi-pane
- 2/3/4-pane layouts with separate splitter memory for each count
- Optional "enlarge active pane" so the pane you're working in gets more room

### Remote and devices
- SFTP · SMB/Samba · FTP · WebDAV — "Connect to Server…" in the sidebar
- Android (MTP), cameras and network mounts listed automatically
- Windows: read files from Linux EXT4 partitions

### File operations
- Copy/move with a destination picker and a visible queue you can edit
- Select by pattern, "New folder from selection", new file from template
- Compress and extract archives
- Open With that remembers your choice per file type
- File compare, quick preview, built-in text editor

### Everyday touches
- Three custom toolbar buttons you can point at any app or command
- 12 UI languages
- Set as the default file manager — on Windows it can also serve the system Open/Save dialogs

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
