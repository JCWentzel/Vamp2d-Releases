# Vamp2D Studio

Vamp2D Studio is a desktop editor for rigging and animating 2D characters from
layered artwork.

**[Download the latest release](https://github.com/JCWentzel/Vamp2d-Releases/releases)**

The initial **0.1.0 Windows preview** includes the Windows installers below.
Linux and macOS are configured in the automated build workflow; their first
hosted builds are waiting for GitHub to create jobs and are not available yet.

| System | Download |
| --- | --- |
| Windows 10/11, 64-bit | `x64-setup.exe` (recommended) or `.msi` |
| Linux, 64-bit | `.AppImage`, `.deb`, or `.rpm` |
| macOS, Apple Silicon | `aarch64.dmg` |
| macOS, Intel | `x64.dmg` |

Open the installer for your system. On Linux, make the AppImage executable before
launching it (`chmod +x *.AppImage`). Linux packages are built on Ubuntu 22.04;
WebKitGTK 4.1 and a working WebGL-capable graphics driver are required.

The initial desktop builds are unsigned, and Mac builds are not notarized.
Windows SmartScreen or macOS Gatekeeper may ask for explicit approval.

## Learn with Max

1. Download [the offline illustrated guide](docs/user-guide.html) using GitHub's
   **Download raw file** button, then open the HTML in your browser. All screenshots
   are embedded; no internet connection is needed.
2. Download [Max.vamp2d](samples/Max.vamp2d) and open it using **File → Open** in
   Vamp2D Studio.
3. Save a separate working copy before experimenting.

Both files are also attached directly to each desktop release. Use the guide's
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
