# WRS Tile Board

An iPad-first digital tile board for Wilson Reading System lessons.

Live page: https://imjusterin2u.github.io/DigitalSpellingTileBoard/

## What it does
- Sound tiles in Wilson colors, filtered by Step (1–12, following the WRS Scope & Sequence). Steps 7–12 add a second tile tab.
- Syllable, base element, prefix and suffix cards typed with the iPad keyboard or an on-screen letter pad. Space or **Next syllable** starts the next card.
- Card Library of pre-written prefixes, suffixes, Latin bases and Greek forms. **Choose cards** hides the ones you don't want showing.
- **Mark Up** with Apple Pencil.
- **Students**: each student's board, step and theme are saved. Open the same student on two iPads and both show the same board live.
- **Theme**: students can pick a board theme. Tile colors never change.

## Two iPads, one board
1. Teacher iPad: tap the name button (top left), pick or add the student.
2. Student iPad: open the same page and tap the same student.
Tip: `?student=<id>` is added to the address, so a bookmark opens that student's board directly.

## Firebase setup (one time)
Project: `digitalspellingtileboard`. In the Firebase console go to **Realtime Database → Rules**, paste the contents of `database.rules.json`, and **Publish**.
These rules let anyone with the link read and write the `tileboard` folder, so use first names or initials for students.

The page talks to Firebase over its plain REST/streaming API (no Firebase SDK download), so it works even where `gstatic.com` is filtered.

## Editing tiles
In `index.html`, `STEP_INTRO` sets the step each tile appears, `BANK_TABS` sets the layout, and `LIB` holds the library cards.
