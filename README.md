# SIDEQUEST

A static productivity arcade built with HTML, CSS, and vanilla JavaScript. No installation, libraries, frameworks, or build step.

## Run

Open `index.html` in a modern browser, or serve this folder with any static HTTP server. Tasks and rewards save in localStorage on the current browser and origin. There is no account or cross-device synchronization. Clearing site data clears your progress.

## GitHub Pages

1. Upload `index.html`, `style.css`, and `app.js` to a GitHub repository's root.
2. In the repository, go to Settings → Pages.
3. Choose Deploy from a branch, select your branch and `/ (root)`, and Save.
4. Open the Pages URL once deployment completes.

Relative asset paths work on both repository project pages and custom domains. No external services or fonts are required.

## Play loop

- Create dated quests with an optional time and category. Choose a 50, 100, or 150 credit reward.
- Complete quests once to earn credits and XP. Every 500 XP earns a level. Complete quests on consecutive dates to build a streak.
- Complete three quests on the same local calendar date to claim a 150 credit daily bonus.
- Spend 25 credits per round on Dot Chaser, Neon Rush, After Hours Hoops, Bullseye Club, or Lucky Grab. A win awards 40 credits.
- Redeem credits for persistent dashboard color themes, a three-quest double-credit boost, or a collision shield consumed on the next maze/racing round.

Keyboard and pointer/touch controls are supported. Rewards and credits are fictional, browser-local motivation tools. Task reminders are visual; no background notifications are scheduled.

## Changes

- Round 5: Added task editing and deletion of completed quests while preserving earned rewards and challenge history. Completed-task reward amounts cannot be changed.
- Round 5: Added a daily check-in panel on every page, showing all seven prizes, claim status, and the local-midnight countdown. Consecutive days award 25, 35, 50, 60, 75, 100, and 150 credits. Day 3 also gives three double-credit quest completions; day 7 unlocks the gold skin and adds a shield. The cycle repeats after day 7; missing a day starts a fresh cycle without removing previously earned prizes. Claims persist in this browser and can be collected once per local date. No account login, backend verification, or notifications are used.
- Round 5: Made the daily task challenge visible on mobile and clarified the task → reflection → credits → games/power-ups loop. The panel and challenge refresh each minute and when returning to the tab.

- Round 3: Fixed Neon Rush traffic fairness. Each spaced wave leaves an open lane, and that opening changes by at most one lane per wave. At top speed, there is at least 0.67 seconds of clear road between collision windows. The race timer follows active simulation time so background-tab delays cannot skip gameplay. A collision now ends drawing immediately, preserving the game-over screen.
- Round 4: Completing a quest now requires a saved 1–2 sentence reflection describing the result and lesson learned (at least 10 words, up to 600 characters). Clicking the checkbox or canceling the form awards nothing. Completed quests show their saved takeaway; existing progress stays intact. This adds accountability but does not verify real-world completion or prevent editing browser storage.
- Round 4: Added a 450ms cooldown between shots/grabs, initialized game markers before input, made moving markers follow active gameplay time, and checked Dot Chaser collisions immediately after movement. Kept the fair Neon Rush waves. Refined typography, card borders, hover states, mobile spacing, and the completion form.
