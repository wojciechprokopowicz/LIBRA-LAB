# LIBRA Lab v4 — flat upload package

All files are in the repository root. There is no `assets` folder: the approved LIBRA Lab logo is embedded directly inside `index.html`.

## Upload
1. Export a backup from the current app first.
2. Open the `LIBRA-LAB` repository on GitHub.
3. Replace the root files with these files: `index.html`, `manifest.webmanifest`, `sw.js`, `README.md`, `CHANGELOG.md`, and `INDEX-MODEL.md`.
4. Do not create or upload an `assets` folder.
5. Keep GitHub Pages set to deploy from `main` / root.
6. After deployment, close and reopen the app on iPhone. If the old version remains, open the site in Safari and reload.

## Data
The app retains the localStorage key `libra_lab_local_v1` and existing stored data structure. Back up your data before replacing files.

## Notes
The Stress-Rest Index is an experimental heuristic, not a medically validated measure. iCloud sync, Face ID, push notifications and automated Dienstplan PDF extraction are not implemented.
