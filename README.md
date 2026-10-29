# AASTU Study Planner PWA — early development build

## Working in this build
- Responsive dashboard and mobile navigation
- Light/dark theme toggle
- Offline-first local storage
- Tasks: add, edit, complete, delete, priorities, due dates and estimates
- Editable starter timetable
- Course records, confidence/weak topics and weighted GPA estimate
- Focus timer, manual session logging and distraction log
- Weekly reflection
- JSON backup/restore and CSV task export
- PWA manifest and service-worker app-shell caching

## Not connected yet
Google sign-in, cloud sync, AI API, push notifications, attachments, CSV import, printable reports, full semester archiving, assessment-weighted GPA projections and adaptive exam/recovery algorithms still need implementation. The app labels cloud/AI/push as unconfigured; do not treat this as production-ready or use it as the only copy of important records.

## Run locally
Run `python3 -m http.server 8080` in this folder, then open `http://localhost:8080`. Service workers require localhost or HTTPS; opening the HTML file directly will not enable the PWA offline layer.

## Deploy frontend to GitHub Pages
1. Create a repository and upload these files to its root.
2. In Settings → Pages, publish the `main` branch root (or configure a GitHub Actions workflow).
3. Open the resulting HTTPS URL and install from the browser menu on Android.

## Important
GitHub Pages hosts only the frontend. Google authentication, cloud database, AI requests and push notifications require external backend services. Never put private API keys in frontend files. Local records are stored in this browser and can be lost if browser data is cleared; export JSON backups regularly.
