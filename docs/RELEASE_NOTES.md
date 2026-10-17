# ForgeWin 0.3 beta

Build 6 is a beta for testing Windows x64 UEFI installer creation on macOS. Requires macOS 14 or later; includes Apple Silicon and Intel binaries.

**Creating media erases all partitions and all data on the selected physical USB drive.**

## Features

- Native English and Hungarian interface with light and dark appearance.
- Windows 10 and Windows 11 x64 ISO inspection and USB drive information.
- GPT or MBR partitioning with FAT32, for UEFI use.
- Automatic splitting of large `install.wim` files using the bundled wimlib tool.
- Copy progress, operation history and SHA-256 comparison through read-back.
- Finalization, ISO detachment and USB volume unmounting before the safe removal message.
- Preparation test without USB writing, available from the ForgeWin menu.

## Testing scope and limitations

This is a beta, not a claim of compatibility with every PC. Real PC UEFI/Secure Boot startup and Windows installation, physical Intel execution and macOS 14 execution still require validation for this release. Copy verification alone does not prove bootability.

Legacy BIOS, ARM Windows, USB targets over 2 TB and oversized ESD files are unsupported. Temporary space on the Mac is required when splitting WIM images. Preliminary ISO checks do not authenticate Microsoft media or fully validate WIM integrity.

Download the `.dmg` release asset and drag ForgeWin to Applications. The `.sha256` asset allows a checksum comparison. The automatic “Source code” archives contain repository documentation only.

Report problems through Issues, including the app version, Mac and macOS version, source Windows build, USB model, partition scheme and exact error. Remove personal information before sharing diagnostics.
