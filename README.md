# Digital Spelling Tile Board

An iPad-first digital tile board for structured literacy lessons: sound tiles, syllable cards, and prefix, suffix and base element cards.

Live page: https://imjusterin2u.github.io/DigitalSpellingTileBoard/

## What it does
- Sound tiles color-coded by consonant, vowel and welded sound.
- **Teacher Tools → Program**: choose the Wilson Reading System® sequence (tiles appear by Step 1–12, following the WRS Scope & Sequence) or an Open board with every tile. Saved with each student.
- Teacher Tools is also where you add and remove students.
- Syllable, base element, prefix and suffix cards typed with the iPad keyboard or an on-screen letter pad. Space or **Next syllable** starts the next card.
- Card Library of pre-written prefixes, suffixes, Latin bases and Greek forms. **Choose cards** hides the ones you don't want showing.
- **Mark Up** with Apple Pencil.
- **Students**: each student's board, step and theme are saved. Open the same student on two iPads and both show the same board live.
- **Theme**: students can pick a board theme. Tile colors never change.

## Open it like an app (no tabs or address bar)
- **iPad:** in Safari tap Share, then **Add to Home Screen**. Open **Tile Board** from the home screen icon. Pick the student once; it remembers.
- **Laptop or Chromebook:** Teacher Tools → **Full screen**, or Chrome's **Install** option.

## Two iPads, one board
1. Add the student once in **Teacher Tools**.
2. Teacher iPad: tap the name button at the top and pick the student.
3. Student iPad: open the same page and tap the same student.
Tip: `?student=<id>` is added to the address, so a bookmark opens that student's board directly.

## Firebase setup (one time)
Project: `digitalspellingtileboard`. In the Firebase console go to **Realtime Database → Rules**, paste the contents of `database.rules.json`, and **Publish**.
These rules let anyone with the link read and write the `tileboard` folder, so use first names or initials for students.

The page talks to Firebase over its plain REST/streaming API (no Firebase SDK download), so it works even where `gstatic.com` is filtered.

## Editing tiles
This tool is independent and not affiliated with Wilson Language Training. In `index.html`, `PROGRAMS` lists the program options, `STEP_INTRO` sets the step each tile appears, `BANK_TABS` sets the layout, and `LIB` holds the library cards.
