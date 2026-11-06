# Daily Planner for Solopreneurs

A focus-first daily planner for founders who have too many good ideas and not enough hours. Plan the day in timed phases, name the three results that matter, and protect the work that moves the business.

## What's in it
- **North Star**: one line for the result that matters most this quarter, carried into every new day.
- **Today's Big 3**: three results (not tasks) to finish before anything else. Finish all three and the day is won; consecutive won days build a streak.
- **Lead measures**: three daily counters with goals (outreach, sales conversations, content shipped). Rename and re-goal them to fit your business.
- **Needle-mover stars**: star your most important tasks. The stats bar shows how much of the day is on them and warns when admin passes 35% or nothing is starred.
- **Done checkboxes**: tick tasks off; a finished timer marks its task done.
- **Revenue and Clients task types** alongside Thinking, Admin, Health, Creative, Fun and Rest.
- **Time tracking**: the timer records real minutes per task so you can compare estimates to reality.
- **Focus mode**: dims every other task while the timer runs (Settings to turn off).
- **Parking lot** (press **P** anywhere, or the pencil on the timer): capture a distracting thought in seconds, then turn it into a task later.
- **Close day**: end-of-day review (win, lesson, tomorrow's Big 3). "Save and open tomorrow" starts the next day with those Big 3 and resets counters.
- **Founder day template** (default) or the original **Personal drill** template, chosen in Settings and applied on Reset.
- Still here: drag and drop phases and tasks, editable everything, 12-hour time, light/dark theme, pomodoro timer with sounds, export/import, offline use, installable PWA, Firebase sync.

## Host on GitHub Pages
Upload `index.html`, `sw.js`, `manifest.json`, `firebase-config.js` (plus the icons) to a repo, then Settings > Pages > Deploy from branch > `main` / root.

## Turn on cross-device sync (Firebase, free Spark plan)
1. Firebase console: create a project, add a **Web app**, and copy its config into `firebase-config.js`.
2. **Authentication** > Sign-in method: enable **Email/Password** (and **Google** if you like).
3. **Authentication** > Settings > **Authorized domains**: add `YOUR-USERNAME.github.io`.
4. **Firestore Database** > Create database, then **Rules**: paste `firestore.rules` and Publish.
5. Open the app, tap **Sign in**, and use the same account everywhere.

Each date is stored as `users/{uid}/days/{YYYY-MM-DD}`. The Big 3, lead measures, parking lot, and review all live inside that day, so the existing rules and your existing data keep working with no migration. The win streak is counted from days stored on the device you are using.
