# L.Q Ledger

[简体中文](README.md) | English

## Overview

L.Q Ledger is a fully offline personal expense tracker for Windows. It focuses on RMB spending and supports fast entry, category management, search and filters, monthly analytics, budgets, soft deletion, complete JSON backup and restore, and CSV reports. No account or network service is required.

The current release is **v1.3.2**.

## Highlights

- Record an amount, category, location, and note with a compact entry flow.
- Reuse recent categories, copy the previous entry, enter simple amount expressions, and create templates.
- Filter records by month, keyword, category, date, or amount.
- Recover records from soft deletion.
- Review monthly category totals, previous-month comparisons, daily averages, highest-spend days, six-month trends, and budgets.
- Customize categories, templates, locations, theme, and interface density.
- Export complete JSON backups for recovery or migration and CSV files for reporting.

## Install

1. Open [Releases](https://github.com/LQ-FJUT/lq-ledger/releases).
2. Download `L.Q记账_1.3.2_x64-setup.exe`.
3. Run the installer and follow the prompts.

The installer is unsigned, so Windows may show an unknown-publisher warning. Verify the SHA-256 value on the Release page before running it.

## Basic use

1. Enter an expense on the ledger page and save it; the form is ready for the next entry immediately.
2. Use recent categories, templates, and copy-previous-entry to speed up repeated records.
3. Search and filter the record list, or restore a soft-deleted entry.
4. Review spending and budgets on the statistics page.
5. Adjust categories, templates, locations, appearance, and density in Settings.
6. Export a complete JSON backup regularly. CSV is intended for viewing in spreadsheet software and cannot restore the ledger.

## Data and privacy

- Ledger data is stored in a local SQLite database, and normal operation does not connect to the internet.
- External JSON is validated before restore, and the current ledger is backed up automatically first.
- An optional rolling daily-backup directory is supported.
- Normal uninstall does not intentionally delete application data.
- Use a complete JSON export for migration between computers; do not copy the installation or build directories.

## Run from source

You need Node.js, the Rust toolchain, and a Windows build environment.

```powershell
npm install
npm test
npm run build
npm run desktop:dev
```

Build the Windows installer:

```powershell
npm run desktop:build
```

## Release status

This repository contains the final source for v1.3.2, while the installer is distributed through GitHub Releases. Local tests, builds, and isolated smoke checks do not replace clean-Windows acceptance testing for first install, upgrade, offline startup, uninstall data retention, and WebView2 fallback behavior.
