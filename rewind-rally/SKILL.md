---
name: rewind-rally
description: Turn one user-selected UGREEN AI NAS photo album into a ready-to-host party game. Rewind Rally builds rounds with three progressive hints (When, Where, What), a host-only answer key tied to each original photo, and scoring. After a game, it can collect the photos used into a new recap album, only after the user confirms. Use when someone says things like "make a game from our trip photos", "photo quiz for family night", "guess-the-memory game for our class reunion", or "Rewind Rally this album". Read-only on originals; nothing leaves the NAS.
---

# Goal

Turn a photo album the user explicitly selects into a fun, fair, ready-to-host guessing game for a group (family, friends, classmates, club, team). Every hint must come from information the NAS actually returns for that photo, so the host can trust the answer key. Originals are never changed.

# Required input

- **Album (required):** one album the user selects or names. If several albums match, list them and ask the user to pick one. Never fall back to searching the whole library.
- **Players (optional):** "kids", "family", or "adults". Default: "family".
- **Rounds (optional):** 3 to 10. Default: 5.
- **Mode (optional):** `classic`, `time-machine`, `where-in-the-world`, or `mixed`. Default: `mixed`. See [Game modes](references/game-modes.md).
- **Exclusions (optional):** people, dates, or photos the user wants kept out of the game.

# Workflow

1. **Confirm scope.** Restate the album, player group, rounds, and mode in one line. Ask only if the album is unclear.
2. **Gather photos (photo-agent).** Ask the photo expert to list photos in the selected album and return, for each candidate, only what the NAS provides: capture date, place or location label, scene or object labels, and any face or person groups that the user has already named. Do not request photos outside this album.
3. **Pick fair candidates.** Apply the [clue rules](references/clue-rules.md). Remove photos that match user exclusions, look like screenshots or documents, have too little information for three honest hints, or are near-duplicates of a photo already chosen. Spread rounds across different dates and places when possible.
4. **Write rounds.** For each chosen photo write three hints, broad to specific:
   - Hint 1 **When**: season, year, or time of day from the capture date.
   - Hint 2 **Where**: region or kind of place from the location label.
   - Hint 3 **What**: a scene or object label, phrased as a playful clue.
   If a field is missing, replace that hint with one supported by another field, or skip the photo. Never guess names, relationships, or events the NAS did not return.
5. **Self-check.** Re-read every hint against its source data. Remove any hint that gives the answer away early, relies on a guess, or exposes sensitive detail (home address, documents, health, identity numbers, children's full names).
6. **Present the game** in this order:
   - Title and a 3-line host script (how to play, scoring: 3 points on Hint 1, 2 on Hint 2, 1 on Hint 3).
   - Player rounds: "Round N" with Hint 1, Hint 2, Hint 3.
   - **Host-only answer key** (clearly separated): the answer, the original photo file name, date, and place for each round, so the host can open and reveal the photo.
7. **Optional recap album (photo-agent, needs confirmation).** Offer: "Want me to create a new album called 'Rewind Rally - <album name>' with these N photos?" Create it only after the user says yes. This adds references to existing photos; it never copies, edits, or removes originals.
8. **Optional save (knowledge-agent, needs confirmation).** If the user asks to keep the host card, confirm the destination folder and file name first. Never overwrite an existing file without a second explicit yes.

# Completion and failure

- **Success:** report rounds created, photos skipped with a short reason each, and whether a recap album or host card was created (only claim it if the action succeeded).
- **Album not found or not permitted:** say so plainly and list albums the user can choose from.
- **Too few usable photos (fewer than 3):** explain why (for example, no dates or places), and suggest a larger album or `classic` mode.
- **Missing metadata:** use only what exists; never invent details to fill a gap.
- **Confirmation declined:** stop that step, keep the game in chat, and change nothing on the NAS.
- **Privacy:** all processing stays on the user's NAS. Do not share, send, or post album content anywhere unless the user explicitly asks and confirms.
