<p align="center"><img src="Taurus-Search-Selected.png" width="112" alt="Taurus Search"></p>

<h1 align="center">Taurus Search</h1>
<p align="center">Your files. Fewer distractions.</p>
<p align="center">Free native file search and app launcher for the macOS menu bar.</p>
<p align="center"><strong>English</strong> · <a href="README.zh-CN.md">简体中文</a></p>
<p align="center"><a href="https://github.com/BRYWANG06/taurus-search/releases/latest"><strong>Download for Mac →</strong></a> · <a href="https://github.com/BRYWANG06/taurus-search/issues">Report an issue</a></p>
<p align="center">macOS 14+ · Apple silicon &amp; Intel · Version 1.0</p>

Press **Option + Space** to find files, folders, and apps. Taurus Search runs in the menu bar, keeps its index on your Mac, and filters recognized logs, caches, and client-managed storage out of results.

## Why Taurus Search?

- **A compact native panel.** Glass appearance on supported macOS versions, with a fallback for older systems. Drag it to a convenient location and remember its position.
- **Apps first.** Matching applications appear before other results, with their actual icons.
- **Less clutter.** Recognized chat and music client internals stay out of results. An optional setting also hides code files.
- **An index that follows your files.** Background filesystem updates, additional reconciliation, and checks for missing paths before search results and file opening. Existing indexes survive app updates.
- **Name-based search.** Search the item's own name rather than listing everything beneath a matching parent folder. Filename-only mode supports literal character fragments. Common Chinese document queries also recognize selected English aliases.
- **Four interface languages.** English, 简体中文, 繁體中文, and 日本語, plus System Default.

Search covers authorized locations available on the local Mac. Filtering affects search results; it does not delete files.

## Install

1. Download **[Taurus.Search.1.0.dmg](https://github.com/BRYWANG06/taurus-search/releases/download/v1.0/Taurus.Search.1.0.dmg)**.
2. Open the disk image and drag **Taurus Search** into **Applications**.
3. Launch it and choose a search folder or **Search This Mac**. Protected locations require permission from the user in System Settings.

**Current distribution status:** version 1.0 is development-signed and has not been notarized by Apple. macOS may block the first launch. The complete Xcode project is also available as a [source archive](https://github.com/BRYWANG06/taurus-search/releases/download/v1.0/Taurus.Search.1.0-Xcode.zip). Download checksums are provided in [SHA256SUMS.txt](https://github.com/BRYWANG06/taurus-search/releases/download/v1.0/SHA256SUMS.txt).

## Choose your language

**Right-click the menu bar magnifying glass → Settings → Language.** Choose English, 简体中文, 繁體中文, 日本語, or System Default. The app follows the system language unless you choose one explicitly.

## Everyday controls

| Action | Control |
| --- | --- |
| Open or close search | Option + Space, or click the menu bar magnifying glass |
| Open a result | Enter or double-click |
| Show in Finder | Command + Enter |
| Close the panel | Esc, or click outside it |
| Settings and shortcut customization | Right-click the menu bar magnifying glass |

The app stays out of the Dock. Start at login, filename-only mode, hiding code files, sorting, search locations, and shortcut customization are available from its menu. Check for Updates connects to this repository's releases.

## Feedback

Found a missing result, a noisy file type, or a translation problem? [Open an issue](https://github.com/BRYWANG06/taurus-search/issues) with your macOS version and steps to reproduce. Please redact private file names and paths from screenshots.

If Taurus Search makes finding your files easier, a **Star** helps others discover it.

## Build from source

Download the **Taurus.Search.1.0-Xcode.zip** release asset, unzip it, and open `TaurusSearchMac/TaurusSearch.xcodeproj` in Xcode. Select the TaurusSearch scheme and My Mac. The complete app source and tests are in that archive; GitHub's automatically generated “Source code” archives contain this download repository.

```sh
xcodebuild -project TaurusSearchMac/TaurusSearch.xcodeproj -scheme TaurusSearch -configuration Release -derivedDataPath build ARCHS='arm64 x86_64' ONLY_ACTIVE_ARCH=NO CODE_SIGNING_ALLOWED=NO build
```
