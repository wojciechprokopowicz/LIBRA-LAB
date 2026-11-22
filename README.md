# LIBRA Lab — initial functional PWA

This repository is a standalone, separate project. It does not modify the existing Stress-Rest app.

## Run locally
Open `index.html` in a modern browser for a basic local preview. For PWA installation and offline caching, serve the folder over HTTPS or localhost.

## GitHub Pages
1. Create a new repository named `LIBRA-Lab`.
2. Upload the contents of this folder to the repository root.
3. In Settings → Pages, deploy from the `main` branch / root.
4. Open the Pages URL on iPhone Safari → Share → Add to Home Screen.

## Included
- Dashboard with Stress-Rest Index and integrated Advice
- Today’s Overview, expandable
- Practice Log and rehearsal/concert event entry
- Monthly Calendar & Load with manual events
- Morning, Evening and Weekly Check-ins
- Practice Planning
- Performance Mode
- Personal Insights
- Coffee-only Lifestyle Log
- Global Search
- JSON full backup / restore (Replace All), CSV activity export
- Basic print-to-PDF report
- Basic diagnostics
- PWA manifest and service worker

## Important implementation limits
- Data is stored locally in the browser using `localStorage`. It does not sync between devices and is not automatically backed up to iCloud.
- The Stress-Rest Index is explicitly experimental. The initial heuristic is a transparent placeholder for data collection and validation, not a medically validated or calibrated model. The app's initial default value before enough personal data exists is an illustrative baseline, not a measured truth.
- PDF Dienstplan text extraction is not implemented in this offline starter. You can add events manually; a production parser still needs to be integrated and tested against real Dienstplan PDFs.
- Automatic Sunday 19:30 push notifications are not implemented. Reliable push while the app is closed requires a push service/backend and user permission; GitHub Pages alone cannot deliver scheduled push.
- PDF reports use the browser print dialog; a dedicated designed PDF renderer and report archive are future implementation work.
- Face ID and iCloud backup require a native iOS implementation.
- This is a functional first implementation, not yet a production-audited app. Test backup/restore before storing important records.

## Index model
See `INDEX-MODEL.md` for the provisional calculation, assumptions, and validation plan.
