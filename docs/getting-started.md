# Install Nearkeep

[Back to README](../README.md) · [简体中文](./getting-started.zh-CN.md)

## Before you download

| Item | Current release |
| --- | --- |
| Hardware | Apple Silicon Mac; no Intel or Windows package |
| macOS | Deployment target: macOS 14. Published testing: macOS 27.0.1; other versions are not fully validated. |
| Package | Nearkeep.app and a local search model; about 619 MB, plus extraction space |
| Version | 1.0.0, build 20261103.1 |
| Signing | Ad-hoc signed; no Developer ID signature or Apple notarization |

## 1. Download and verify

Get `Nearkeep-1.0.0-macOS-arm64.zip` and `SHA256SUMS.txt` from the [official release](https://github.com/jayueseven/Nearkeep/releases/tag/v1.0.0). Put them in one folder. Open Terminal in that folder and run:

```sh
shasum -a 256 -c SHA256SUMS.txt
```

The ZIP filename should be followed by `OK`. A checksum verifies download integrity; it does not replace notarization or a security audit.

The November 12, 2026 package refresh uses the same version and build identifier as the previous package. Use the current checksum on the release page to distinguish them.

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

- Record a quick-search shortcut in Settings. Nearkeep must be running for the shortcut to work.
- Previews use macOS Quick Look, so format support depends on the system. Common image thumbnails include JPEG/JPG, PNG, HEIC, TIFF, GIF, BMP and WebP. Animated images use a still frame; corrupt or unsupported files may not preview. Temporary failures have limited retries and a manual retry action.
- The default save location detects Finder additions, moves and renames. Large folders may take time to synchronize. See the [release notes](https://github.com/jayueseven/Nearkeep/releases/tag/v1.0.0) for scanning limits and older-file behavior.
- Updates are manual through [Releases](https://github.com/jayueseven/Nearkeep/releases). Quit first, back up important files and keep your storage location. Not every historical upgrade or downgrade path has been validated.
- Do not run multiple Nearkeep versions together. Local development and distribution builds currently share a data identity.

[Search and privacy details](./search-and-privacy.md) · [Report an issue](https://github.com/jayueseven/Nearkeep/issues)
