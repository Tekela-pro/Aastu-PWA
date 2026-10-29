# AASTU Study Planner PWA — Academic Engine Update

An offline-first study planner for AASTU students. This version adds a stronger academic-record workflow while keeping the app static-hostable on GitHub Pages.

## Included
- Responsive dashboard and mobile navigation
- Light/dark theme
- Offline-first local storage and service-worker app shell
- Tasks: add, edit, complete, delete, priority, due date, time estimate
- Editable starter timetable (verify all class times against the official timetable)
- Semester creation, selection, and renaming
- Courses with credits, confirmed grade points, projected grade points, confidence, and weak-topic notes
- Assessment records per course: quiz, assignment, midterm, final, lab, project, or other; score, maximum score, weight, and optional date
- Assessment-derived percentage and grade-point estimate when a confirmed grade point is not entered
- Editable percentage-to-grade-point scale
- Current semester weighted GPA and projected GPA
- Focus timer, manual session logging, distraction log, and weekly reflection
- JSON backup/restore and CSV task export
- PWA manifest and service-worker caching

## Important academic accuracy notes
- The built-in grading scale is an **editable example**, not verified AASTU policy. Replace it with the official scale used by your courses before relying on assessment-derived grade points.
- A manually entered confirmed grade point takes precedence over the assessment-derived estimate for that course.
- Assessment percentages are calculated from the assessments entered so far, normalized by their entered weights. Add each assessment's actual course weight, and keep total weights at or below 100%.
- GPA is weighted by the course credits you enter. Make sure credits, grade points, and semester assignments match your official records.
- GPA projections are estimates, not guarantees. A blank projected grade uses the current grade estimate for that course.
- Starter timetable entries are editable examples and should be checked against the official AASTU timetable.

## Not connected yet
Google sign-in, cloud sync, AI API, push notifications, file attachments, CSV import, printable reports, and advanced adaptive exam/recovery algorithms still require further development. GitHub Pages hosts only the static frontend; cloud features require external services. Do not put private API keys in frontend files.

## Run locally
Run `python3 -m http.server 8080` in this folder, then open `http://localhost:8080`. Service workers require localhost or HTTPS; opening `index.html` directly will not enable the PWA offline layer.

## Deploy/update on GitHub Pages
Upload the **contents** of this folder to the repository root, replacing the previous version. Keep `index.html`, `app.js`, `styles.css`, `sw.js`, `manifest.webmanifest`, and the `icons` folder together. In GitHub, commit the changed files. If the site appears unchanged, close and reopen it or refresh after the service-worker update.

## Backup warning
Your records are stored in this browser on this device. Export a JSON backup regularly, especially before clearing browser data or switching devices.
