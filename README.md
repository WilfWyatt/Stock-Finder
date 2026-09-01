# Stock Finder

A simple, installable web app for searching warehouse stock by product code, description, or location — built for personal use, no app store required.

## Features

- Live search across **item code** and **description**
- Separate search field for **location**
- Loads stock data directly from an Excel spreadsheet (`.xlsx`) — no conversion needed
- Installable to your phone's home screen as a standalone app (works offline after first load)
- Clean, dark, high-contrast UI designed for quick scanning

## Usage

1. Open the app
2. Tap **Load File** and select your stock spreadsheet
3. Search by code/description, location, or both at once

## Expected spreadsheet columns

The app reads the first sheet of the uploaded file and expects these column headers:

| Column | Used for |
|---|---|
| `Item` | Product code |
| `Item Description` | Product name/description |
| `Locator` | Storage location |
| `Primary UOM` | Unit of measure badge |

To match different column names, edit the `COLUMNS` object near the top of the `<script>` block in `index.html`.

## Installing as an app

1. Open the live site in Chrome on Android
2. Tap the **⋮** menu → **Install app**
3. Launch it from your home screen — full screen, no browser bar

## Files

- `index.html` — the app itself
- `manifest.json` — app name, icon, and display settings for installability
- `service-worker.js` — caches the app for offline use after first load
- `icon-192.png`, `icon-512.png`, `icon-512-maskable.png` — home screen icons

## Tech

Plain HTML/CSS/JS, no build step. Spreadsheet parsing via [SheetJS](https://sheetjs.com/).
