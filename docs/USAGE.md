# ForgeWin usage notes

ForgeWin creates Windows x64 UEFI installation media from a local ISO. Use a USB drive whose entire contents may be erased, and check its model and capacity before confirming.

## Before writing

ISO selection starts a preliminary check. This checks supported installer structure and preparation requirements; it does not authenticate Microsoft media or perform a complete WIM integrity check. Obtain your ISO from Microsoft.

Use the information buttons to inspect the source image and target drive. The app only offers external physical USB targets and checks drive identity before erasing. These protections do not replace choosing the correct drive.

The ForgeWin menu includes a preparation test without USB writing. It can split a large WIM using temporary space on the Mac and stops before formatting.

## While creating

Large WIM files are prepared before USB erasure. The target is then formatted, files are copied and checked by reading them back, and the media is finalized.

Keep the Mac awake and the USB attached. Cancel is unavailable during formatting and finalization. Cancellation after erasure has started cannot restore the old contents. If an operation fails, the drive may contain an incomplete installer; start again after resolving the error.

After successful finalization, ForgeWin detaches the source ISO and unmounts the USB volumes. Wait for the safe removal message. The Eject button ejects the whole physical USB drive.

## Limits and troubleshooting

- GPT and MBR options both target x64 UEFI use. MBR does not add Legacy BIOS support.
- USB drives over 2 TB are unsupported.
- Files exceeding FAT32's size limit are rejected unless they are a supported WIM image that can be split. Oversized ESD files are not split.
- A successful copy verification does not establish UEFI, Secure Boot or Windows installation compatibility with a specific PC.
- If macOS prevents the app from opening, keep the exact message for your report. Do not disable Gatekeeper or remove quarantine as a workaround.
- On a preparation, permission or system error, use the app's Last Error and History windows. ForgeWin does not ask for or store an administrator password.

For feedback, include the version, Mac model/chip, macOS version, ISO version/build and architecture, USB model/capacity, GPT or MBR choice, the failed step and exact error. When testing on a PC, include the UEFI/Secure Boot settings and whether Windows Setup starts. Remove personal paths, filenames and unrelated information before sharing logs.
