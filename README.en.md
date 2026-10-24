# PickAbc

<a href="https://github.com/joseygo/PickAbc/releases/latest">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/badge-download-en-dark.svg">
    <img src="assets/badge-download-en.svg" alt="Download PickAbc · Windows 10/11" height="30">
  </picture>
</a>

**English** · [简体中文](README.md)

An always-on-top text panel: save the phrases you use every day, click once to copy.

![PickAbc](design/pickabc-ui.png)

## Download and run (Windows 10 / 11)

Grab `PickAbc-1.0.2-win64.zip` from
[Releases](https://github.com/joseygo/PickAbc/releases), unzip it, and double-click
`PickAbc.exe`. No Python, no installer, no internet connection, no third-party dependencies.
Single file, about 9.5 MB.

## How to use

| Action | Result |
|---|---|
| Click a text | Copy it to the clipboard |
| Drag a text out | Drop it on any input box in any app — it gets pasted there |
| Drag text in from elsewhere | Drop it anywhere on the panel to open "Add text" pre-filled |
| Right-click it | Menu: edit |
| Language menu (top right) | Switch the interface language: English / Deutsch / 简体中文 |
| Type 111~999 in any app | A confirm bar pops up; press Enter to erase the digits, copy the matching text and paste it (global quick input) |
| ＋ at the bottom right | Add a text |
| "Delete" inside the editor | Remove that text |

The window stays on top by default. Only one instance runs at a time — if it is already
open, double-clicking the exe again just brings the existing window to the front.

## Where your data lives

Your texts are stored in `%APPDATA%\PickAbc`, so updating the app never loses them:

```
%APPDATA%\PickAbc\snippets.json    # texts
```

**Portable mode**: drop an empty file named `portable.flag` next to `PickAbc.exe` and the
data will be kept beside the exe instead.

## Features

- **First run** — ships with 4 example texts; if you delete them all, they are not restored

## About iOS

This app is built on Python + Tkinter, a desktop framework, and **cannot be packaged for iOS**:
iOS does not allow running a Python interpreter and requires native UIKit apps. It will not
run on iPhone / iPad.

On a phone you can get a similar effect with the built-in **Text Replacement**
(Settings → General → Keyboard → Text Replacement).

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
source distribution and sublicensing are not permitted. This repository is the private
development repository.

© 2026 Josey. All rights reserved.
