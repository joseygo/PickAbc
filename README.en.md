# PickAbc

<a href="https://github.com/joseygo/PickAbc/releases/latest">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/badge-download-en-dark.svg">
    <img src="assets/badge-download-en.svg" alt="Download PickAbc · Windows 10/11" height="30">
  </picture>
</a>

**English** · [简体中文](README.md)

An always-on-top text panel: save the phrases you use every day, copy one with a single
click — or drag it straight into any input box.

![PickAbc](design/pickabc-ui.png)

## Download and run (Windows 10 / 11)

Grab `PickAbc-1.0.1-win64.zip` from
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
| Type 111~999 in any app | A confirm bar pops up; press Enter to erase the digits, copy the matching text and paste it (global quick input) |
| ＋ at the bottom right | Add a text |
| "Delete" inside the editor | Remove that text |
| Sort icon at the top right | Reorder by usage |

The window stays on top, docked to the left edge, a fixed quarter of the screen wide and
vertically resizable. Only one instance runs at a time — if it is already open,
double-clicking the exe again just brings the existing window to the front.

## Where your data lives

Your texts are stored in `%APPDATA%\PickAbc`, so updating the app never loses them:

```
%APPDATA%\PickAbc\snippets.json    # texts
```

**Portable mode**: drop an empty file named `portable.flag` next to `PickAbc.exe` and the
data will be kept beside the exe instead.

## Features

- **First run** — ships with 4 example texts; if you delete them all, they are not restored
- **Global quick input** — type three identical digits (111~999) in any app to insert that text
- **Drag both ways** — drag texts out to other apps, drag selected text in from other apps

## About iOS

This app is built on Python + Tkinter, a desktop framework, and **cannot be packaged for iOS**:
iOS does not allow running a Python interpreter and requires native UIKit apps. It will not
run on iPhone / iPad.

On a phone you can get a similar effect with the built-in **Text Replacement**
(Settings → General → Keyboard → Text Replacement).

## Requirements

- Windows 10 / Windows 11 (64-bit)
- No administrator rights, no registry writes, no background service

## Known warning

The first launch may trigger Windows SmartScreen ("Windows protected your PC"). This is normal
for an indie project without a code-signing certificate (which costs thousands of dollars a
year). Click **More info** → **Run anyway**.

## Copyright & License

PickAbc is **closed-source software**. This repository only distributes pre-built Windows
executables and usage notes; the source code is not provided, and redistribution or
sublicensing of the source is not permitted.

© 2026 Josey. All rights reserved.
