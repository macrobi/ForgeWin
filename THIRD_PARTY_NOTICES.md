# Third party notices

## wimlib 1.14.5

ForgeWin invokes `wimlib-imagex` as a separate command-line process to read Windows image metadata and split WIM files.

Upstream project: [wimlib](https://wimlib.net/).

The CLI is licensed under **GPL-3.0-or-later**. Upstream copyright notices and licensing terms are preserved in its source archive and license files. ForgeWin's copyright notice does not replace these terms.

The application includes the following in `ForgeWin.app/Contents/Resources/Tools`:

- `COPYING`, `COPYING.GPLv3` and `COPYING.LGPL`;
- the complete, unmodified `wimlib-1.14.5.tar.gz` upstream source archive;
- `build-wimlib.sh`, the rebuild script;
- `README.md`, describing provenance and rebuilding.

In Finder, right-click ForgeWin and select **Show Package Contents** to access them. The bundled executable is at `Contents/MacOS/wimlib-imagex`.

Source archive SHA-256:

```text
84221a3abd5b91228f15f8e6065c335a336237b5738197b75bf419eea561a194
```

To rebuild the helper, copy the source tree to a directory whose entire absolute path contains no spaces, then follow the included README. This is a requirement of the upstream build tooling. The script builds arm64 and x86_64 variants for macOS 14 or later using Xcode command-line tools and the macOS SDK, with static libwim and without ntfs-3g or FUSE.

## Microsoft names

Windows and Microsoft are trademarks of the Microsoft group of companies. ForgeWin is not a Microsoft product. No Windows ISO or Windows license is included.
