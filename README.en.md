# L.Q Ledger

[简体中文](README.md) | English

**A personal expense tracker with no account and no network connection during everyday use.**

Record spending quickly, review categories and monthly trends, set budgets and keep your own backups.

The current Windows release is **1.3.2**. An Android ARM64 preview package is also available. [Download](https://github.com/tukitohosi/lq-ledger/releases/tag/v1.3.2)

## Features

- Fast entry with recent categories, location suggestions, copy-previous-entry, amount expressions and templates.
- Filters for month, keyword, category, date and amount.
- Category totals, previous-month comparisons, daily averages, highest-spend days and six-month trends.
- Custom categories, category merging and category budgets.
- Complete JSON backup and restore, CSV reports and optional rolling daily backups.
- Light/dark themes, comfortable/compact layouts and keyboard controls.

## Install

Choose a package from the [v1.3.2 release](https://github.com/tukitohosi/lq-ledger/releases/tag/v1.3.2):

- Windows x64: LQ-Ledger-1.3.2-x64-Setup.exe.
- Android 7.0+ ARM64 preview: LQ-Ledger-1.3.2-Android-arm64-debug.apk.

If WebView2 is missing, setup can download it from Microsoft; everyday operation is offline.

The Android package uses a Debug signing key and is a preview. Its Android build changes are not included in the v1.3.2 source tag. Use the platform-specific checksums on the release page.

## Data and limitations

The app is for one person's RMB expenses. Amounts are stored as integer cents in a local SQLite database.

Use complete JSON exports for backups and migration. Restore automatically backs up the current ledger first. CSV is a report format and cannot restore the ledger. A normal Windows uninstall keeps application data; an optional daily-backup folder can be selected in Settings.

## Run from source

Requires Node.js, Rust and a Windows build environment.

~~~powershell
npm install
npm run desktop:dev
~~~
