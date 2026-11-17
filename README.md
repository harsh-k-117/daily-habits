# ☕ Daily: a private habit and focus tracker

Daily is a calm, monochrome habit tracker built as a single HTML file. It combines streaks, a focus timer, one-off tasks, weekly reviews and detailed analytics, and it keeps everything in your browser. There is no server, no account and no tracking.

**Live demo:** `https://YOUR-USERNAME.github.io/YOUR-REPO/` <!-- Replace after deploying -->

<!--
Add screenshots after you deploy, then uncomment:

![Today page](screenshots/today.png)
![Progress page](screenshots/progress.png)
-->

## Why it exists

Most habit apps reward perfection and punish a missed day. Daily is built around a different idea: show up, keep the floor, and never miss twice. Every habit can have a minimum version for bad days, rest days pause a streak without breaking it, and success is defined by showing up rather than by how well the session went.

## Features

**Today**
- Cup progress indicator that fills as you finish habits, with a live streak.
- One-tap "Start with…" button that picks your next unfinished habit (core habits first) and starts the focus timer.
- Habit checklist with a "bad day" minimum version and per-habit streaks.
- One-off tasks for anything that is not a recurring habit.
- Daily log with a 1 to 5 energy rating and a short note.
- Coming up: countdowns to exams, deadlines and other key dates.
- Rest day toggle that pauses the streak instead of breaking it.

**Focus timer**
- Presets of 15, 30, 45 and 60 minutes, plus a custom length from 1 to 240 minutes.
- Sessions started from a habit are logged against that habit.
- Stop early and keep the minutes you actually focused.
- Optional sound when a session ends.

**Progress and analytics**
- Time range of 7, 30 or 90 days.
- Summary tiles: consistency, completion rate (with change versus the previous period), streak and best streak, perfect days, focus time and average energy.
- 16-week activity heatmap and an editable month calendar.
- Weekly completion, completion by weekday, focus minutes and energy charts.
- Habit breakdown with completion, current and best streak, and focus time.
- Generated insights, such as your strongest weekday, weakest habit and energy patterns.
- Weekly review with notes from previous weeks.
- CSV export and a print-friendly report.

**Settings and data**
- Add, edit, reorder and delete habits, with a choice of days and a core flag.
- Key dates, timer sound and keyboard shortcut preferences.
- JSON backup download, file import, copy-and-paste backup, and undo for destructive actions.

## Quick start

No build step and no dependencies.

1. Download `index.html`.
2. Open it in a modern browser.

An internet connection is needed once to load the Geist font from Google Fonts. Without it, the page falls back to your system font.

## Deploy with GitHub Pages

1. Create a new **public** repository (free GitHub Pages sites require a public repository).
2. Add `index.html` and `README.md` to the root of the repository.
3. Go to **Settings → Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**, choose the `main` branch and the `/ (root)` folder, and click **Save**.
4. Wait a few minutes, then open `https://YOUR-USERNAME.github.io/YOUR-REPO/`.

Updating the site is just a new commit that replaces `index.html`.

## Keyboard shortcuts

| Key | Action |
| --- | --- |
| `1` to `9` | Toggle the matching habit on the selected day |
| `T` `P` `S` | Go to Today, Progress or Settings |
| `?` | Open help |

Shortcuts can be turned off in Settings.

## Data and privacy

- All data is stored in your browser's `localStorage`. Nothing is sent anywhere.
- Data belongs to the browser and address where you used the app. A copy opened from your computer and the hosted version keep separate data, so use **Settings → Your data → Download backup** and **Import file** to move between them.
- Clearing site data deletes your history, so download a backup now and then.
- A Content-Security-Policy meta tag restricts the page to inline scripts, inline styles and Google Fonts.

## Tech notes

- One self-contained HTML file with inline CSS and vanilla JavaScript. No framework and no build tooling.
- Geist and Geist Mono via Google Fonts, with system font fallbacks.
- Light and dark monochrome themes that follow your device setting.
- Responsive from small phones to wide desktops, with a bottom tab bar on phones and safe-area support for notched devices.
- Accessibility basics: skip link, semantic landmarks, visible focus states, keyboard support, reduced-motion support and larger tap targets on touch devices.
- Data is versioned and validated on load and import, and changes sync across open tabs.

**Browser support:** recent versions of Chrome and Edge (111+), Safari (16.2+) and Firefox (113+). The page uses `color-mix()` and the `<dialog>` element.

## Project structure

```
.
├── index.html     # The entire app
├── README.md
└── screenshots/   # Optional, for the README
```

## Roadmap ideas

- Installable app support (manifest and service worker)
- Optional sync between devices
- Habit targets beyond daily check-offs
- Additional export formats

## License

Add a license when you create the repository (the MIT License is a common choice for personal projects) and update this section.
