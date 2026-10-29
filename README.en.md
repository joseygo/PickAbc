# PickAbc

<a href="https://github.com/joseygo/PickAbc/releases/latest">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/badge-download-en-dark.svg">
    <img src="assets/badge-download-en.svg" alt="Download PickAbc · Windows 10/11" height="30">
  </picture>
</a>

**English** · [简体中文](README.md)

An always-on-top text panel: save the phrases you use every day and double-click to copy.
Tuck it into the screen edge when you don't need it — only a thin strip stays visible.

![PickAbc](design/pickabc-ui.png)

## Download and run (Windows 10 / 11)

Grab `PickAbc-1.0.5-win64.zip` from
[Releases](https://github.com/joseygo/PickAbc/releases), unzip it, and double-click
`PickAbc.exe`. No Python, no installer, no internet connection, no third-party dependencies.
Single file, about 10 MB.

## How to use

| Action | Result |
|---|---|
| Double-click a text | Copy it to the clipboard (a single click does nothing, to avoid misfires) |
| Drag a text out | Drop it on any input box in any app — it gets pasted there |
| Right-click it | Menu: edit |
| "Hide" icon (top left) | Tuck the whole panel into the left edge in one click, leaving only a thin strip |
| Drag the window to the left edge and let go | The whole panel slides off-screen and only a thin strip marked **P** stays on the left edge; hover the strip to bring it back, move the cursor away for about a second and it hides again |
| Sort icon (top right) | Reorder the list by how often each text was used (copy, quick input, drag-out), highest first |
| Gear icon (top right) → settings | Interface language (English / Deutsch / Español / 简体中文) · Launch at Windows startup · Check for updates · Email |
| Tap the same digit twice quickly (11~99) in any app | A confirm bar pops up; press Enter to erase the digits, copy the matching text and paste it (global quick input) |
| ＋ at the bottom right | Add a text |
| ✓ or `Ctrl+S` inside the editor | Save your changes (Enter inserts a newline, it does not save) |
| "Delete" inside the editor | Remove that text |

The window stays on top and docked to the left edge of the screen, and its bottom edge never
covers the taskbar. Only one instance runs at a time — if it is already open, double-clicking
the exe again just brings the existing window to the front.

## Where your data lives

Your texts are stored in `%APPDATA%\PickAbc`, so updating the app never loses them:

```
%APPDATA%\PickAbc\snippets.json    # texts
```

**Portable mode**: drop an empty file named `portable.flag` next to `PickAbc.exe` and the
data will be kept beside the exe instead.

## Features

- **First run** — ships with 5 example texts and an English interface (switch the language from
  the gear menu; the choice is remembered); if you delete them all, they are not restored
- **Launch at startup** — a toggle in the gear menu. Nothing is written to the registry; just
  delete the exe to uninstall, and Windows startup will no longer report a missing file

## Requirements

- Windows 10 / Windows 11 (64-bit)
- No administrator rights, no registry writes, no background service

## Build it yourself (optional)

The source is a single file, `PickAbc.py`, standard library only (Python 3 + Tkinter).
Run it locally:

```
pythonw PickAbc.py
```

Package it into an exe:

```
pip install pyinstaller
python -m PyInstaller PickAbc.spec --noconfirm --clean
```

The result lands in `dist/PickAbc.exe`.

## Known warning

The first launch may trigger Windows SmartScreen ("Windows protected your PC"). This is normal
for an indie project without a code-signing certificate (which costs thousands of dollars a
year). Click **More info** → **Run anyway**.

## Copyright & License

PickAbc is **closed-source software**. Only pre-built Windows executables are distributed;
source distribution and sublicensing are not permitted. This repository publishes the docs and
prebuilt binaries only — it contains no source code.

© 2026 Josey. All rights reserved.
