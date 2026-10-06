# Daily Drill Planner

Installable daily planner: timed drills in phases, drag drills and phases to rearrange (times reflow automatically), 12-hour time, everything editable, light/dark theme, drill timer with optional pomodoro cycles and selectable sounds, and a settings panel (gear icon) for theme, timer, sounds, account, export, import and reset. Works fully offline on one device; add Firebase to sync across devices.

## Host on GitHub Pages
Upload `index.html`, `sw.js`, `manifest.json`, `firebase-config.js` to a repo, then Settings > Pages > Deploy from branch > `main` / root.

## Turn on cross-device sync (Firebase, free Spark plan)
1. Firebase console: create a project, then add a **Web app** and copy its config into `firebase-config.js`.
2. **Authentication** > Sign-in method: enable **Email/Password** (and **Google** if you like).
3. **Authentication** > Settings > **Authorized domains**: add `YOUR-USERNAME.github.io`.
4. **Firestore Database** > Create database (production mode), then **Rules**: paste the contents of `firestore.rules` and Publish.
5. Commit the updated `firebase-config.js`. Open the app, tap **Sign in**, and use the same account on every device.

Each date is stored as `users/{uid}/days/{YYYY-MM-DD}`. Edits sync live; if two devices edit the same day, the most recent edit wins. Offline edits are kept on the device and upload when you reconnect.
