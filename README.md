# Vamp2D Studio

Vamp2D Studio is a desktop editor for rigging and animating 2D characters from
layered artwork.

**[Download Vamp2D Studio 0.1.0](https://github.com/JCWentzel/Vamp2d-Releases/releases/tag/v0.1.0)**

Desktop installers are available for Windows x64, Linux x64, and macOS on both
Apple Silicon and Intel processors.

| System | Download |
| --- | --- |
| Windows 10/11, 64-bit | [Setup EXE](https://github.com/JCWentzel/Vamp2d-Releases/releases/download/v0.1.0/Vamp2D.Studio_0.1.0_x64-setup.exe) (recommended) · [MSI](https://github.com/JCWentzel/Vamp2d-Releases/releases/download/v0.1.0/Vamp2D.Studio_0.1.0_x64_en-US.msi) |
| Linux, 64-bit | [AppImage](https://github.com/JCWentzel/Vamp2d-Releases/releases/download/v0.1.0/Vamp2D.Studio_0.1.0_amd64.AppImage) · [DEB](https://github.com/JCWentzel/Vamp2d-Releases/releases/download/v0.1.0/Vamp2D.Studio_0.1.0_amd64.deb) · [RPM](https://github.com/JCWentzel/Vamp2d-Releases/releases/download/v0.1.0/Vamp2D.Studio-0.1.0-1.x86_64.rpm) |
| macOS, Apple Silicon | [ARM64 DMG](https://github.com/JCWentzel/Vamp2d-Releases/releases/download/v0.1.0/Vamp2D.Studio_0.1.0_aarch64.dmg) |
| macOS, Intel | [Intel DMG](https://github.com/JCWentzel/Vamp2d-Releases/releases/download/v0.1.0/Vamp2D.Studio_0.1.0_x64.dmg) |

Open the installer for your system. On Linux, make the AppImage executable before
launching it (`chmod +x *.AppImage`). Linux packages are built on Ubuntu 22.04;
WebKitGTK 4.1 and a working WebGL-capable graphics driver are required.

These desktop builds are unsigned, and Mac builds are not notarized.
Windows SmartScreen or macOS Gatekeeper may ask for explicit approval.

## Learn with Max

1. Download [the offline illustrated guide](https://github.com/JCWentzel/Vamp2d-Releases/releases/download/v0.1.0/user-guide.html),
   then open the HTML in your browser. All screenshots
   are embedded; no internet connection is needed.
2. Download [Max.vamp2d](https://github.com/JCWentzel/Vamp2d-Releases/releases/download/v0.1.0/Max.vamp2d) and open it using **File → Open** in
   Vamp2D Studio.
3. Save a separate working copy before experimenting.

Repository copies: [guide](docs/user-guide.html) · [Max](samples/Max.vamp2d). Use the guide's
**Print / Save PDF** button for a printable copy.

## Verify downloads

Each release includes `SHA256SUMS.txt` and `release-manifest.json`, recording the
build revision and checksums. For example, in PowerShell:

```powershell
Get-FileHash './Vamp2D.Studio_0.1.0_x64-setup.exe' -Algorithm SHA256
```

Compare the hash with the matching entry in `SHA256SUMS.txt`.

This repository contains distribution files and sample artwork. Desktop builds
are produced by the app's source repository using GitHub Actions on Windows,
Linux, and macOS. Publishing is handled by the source repository's
`pnpm release:desktop <version>` command.
