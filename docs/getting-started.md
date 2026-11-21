# Install Nearkeep on macOS

[Back to README](../README.md) · [简体中文](./getting-started.zh-CN.md)

On Windows? See the [Windows x64 download and installation instructions](https://github.com/jayueseven/Nearkeep/releases/tag/v1.0.1-windows).

## Before you download

| Item | Current release |
| --- | --- |
| Hardware | Apple Silicon Mac; no Intel Mac package |
| macOS | Deployment target: macOS 14. See the [macOS release](https://github.com/jayueseven/Nearkeep/releases/tag/v1.0.1) for test coverage. |
| Package | Nearkeep.app and a local search model; about 619 MB, plus extraction space |
| Version | 1.0.1, build 20261119.1 |
| Signing | Ad-hoc signed; no Developer ID signature or Apple notarization |

## 1. Download and verify

Get `Nearkeep-1.0.1-macOS-arm64.zip` from the [official release](https://github.com/jayueseven/Nearkeep/releases/tag/v1.0.1). Open Terminal in the download folder and run:

```sh
shasum -a 256 'Nearkeep-1.0.1-macOS-arm64.zip'
```

The checksum should match `3dde4df44400fc11ce7a1e8d317ba7668a07482876d612a9164d592243412072`. A checksum verifies download integrity; it does not replace notarization or a security audit.

Version 1.0.1 has its own tag, package and build identifier. The 1.0.0 release notes are available for reference.

## 2. Install and open

Extract the ZIP and move **Nearkeep.app** to Applications. If updating, quit the older app normally before replacing it. Keep your existing Library storage folder.

The current app is not notarized, so macOS may block the first launch. After verifying the source and checksum, follow [Apple's guidance](https://support.apple.com/en-us/102445) for the specific warning. Do not disable system-wide protections. Stop and report warnings about malware, damage or corruption.

## 3. Choose where files live

A fresh setup opens an empty Library and asks you to choose a dedicated storage folder. Cancelling does not start an import. Existing users keep their Library and chosen storage location.

Import files with Upload, drag them into the Library, or drop them onto desktop Nicole. Choose:

- **Copy:** save a separate copy and keep the original.
- **Move:** remove the source only after a successful safe save. Sources containing recognized Nearkeep internal metadata are retained, with a notice.
- **Link an existing folder in Settings:** manage files in their current location without importing copies. Renaming, moving or deleting linked items affects the originals. Unlinking keeps the files.

Nested and empty folders are preserved. After import, choose View to locate the items or Done to close the receipt.

## Using and updating your Library

- Record or clear shortcuts in Settings. Library visibility and quick search are global while Nearkeep is running. Nicole visibility works only with the Library window active and Settings and other dialogs closed.
- Previews use macOS Quick Look, so format support depends on the system. Common image thumbnails include JPEG/JPG, PNG, HEIC, TIFF, GIF, BMP and WebP. Animated images use a still frame; corrupt or unsupported files may not preview. Temporary failures have limited retries and a manual retry action.
- The default save location detects Finder additions, moves and renames. Large folders may take time to synchronize. See the [release notes](https://github.com/jayueseven/Nearkeep/releases/tag/v1.0.0) for scanning limits and older-file behavior.
- Updates are manual through [Releases](https://github.com/jayueseven/Nearkeep/releases). Quit first, back up important files and keep your storage location. Not every historical upgrade or downgrade path has been validated.
- Do not run multiple Nearkeep versions together. Local development and distribution builds currently share a data identity.

[Search and privacy details](./search-and-privacy.md) · [Report an issue](https://github.com/jayueseven/Nearkeep/issues)

