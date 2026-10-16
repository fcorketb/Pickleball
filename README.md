# Courtside Pickleball

A free, mobile-friendly app for running social pickleball round robins: check in players,
generate a fair schedule across your courts, enter scores courtside and watch a live leaderboard.

- Rotating partners (or fixed teams) with as few repeat partners and opponents as possible
- Fair rests when there are more players than court spaces
- Big score keypad, undo, and edits to finished matches
- Live standings with adjustable ranking rules, and player history across sessions
- Courtside display mode for a tablet at the court
- Works fully offline once installed to a phone's home screen

## Your data

Everything (players, sessions, results) is stored **on the organiser's device only**.
This repository contains the empty app and no player data.

- Use **History → Save backup** after each session and keep the file in your cloud storage.
- Use **History → Restore from backup** to load it on another device.
- **Never upload backup `.json` files to this repository.** They contain players' names.
  `.gitignore` blocks them by default.

## Adding your own logo

Two ways:

1. **For everyone:** replace `logo.svg` in this repository with your own logo (keep the same name).
   To use a PNG instead, upload it as `logo.png` and change `LOGO_FILE` near the top of the script
   in `index.html` from `'logo.svg'` to `'logo.png'`, and the same name in `sw.js`.
2. **On one device:** tap the logo in the app and choose an image. It's saved on that device and
   included in its backups.

The home-screen icons are `icon-192.png`, `icon-512.png`, `icon-maskable-512.png` and
`apple-touch-icon.png`. Replace them with your own images of the same sizes to change the app icon.

## Deploying on Vercel

1. In Vercel, choose **Add New → Project** and pick this repository.
2. Framework preset: **Other**. Leave the build command and output directory empty.
3. Click **Deploy**. Every change pushed to `main` redeploys automatically.

## Publishing an update

After changing files, open `sw.js` and bump `VERSION` (for example `courtside-v2`).
Installed copies pick up the update the next time they open with signal.
