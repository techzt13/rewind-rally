---
name: rewind-rally
description: Create a family-friendly, source-grounded guessing game from a user-selected UGREEN NAS photo album. Use when someone wants to play a photo-memory game with a group.
---

# Goal

Turn a photo album the user explicitly selects into a ready-to-host group guessing game. Make progressive clues and an answer key that points to the original photos. Keep the game playful, accessible, and grounded in information available from the selected album.

# Required input

- A specific NAS photo album selected or clearly identified by the user.
- The intended audience or tone. If omitted, use family-friendly language suitable for a mixed-age group.
- The number of rounds. If omitted, make five; do not make more than ten in one game.

If the album is ambiguous, ask the user to choose one before searching. Do not search other albums or the wider NAS as a substitute.

# Workflow

1. Use only the available UGREEN NAS album and photo capabilities, and only on the album the user selected. Do not invent tool names, capabilities, photo details, identities, or relationships.
2. Gather a small set of candidate photos and the descriptions or metadata that the available NAS capabilities actually return. Prefer distinct, clearly supported moments. Do not infer sensitive traits or identify people unless the user supplied that information.
3. Make one round per usable photo. Each round should contain two or three clues, revealed one at a time, that progress from broad to specific. Include the answer and a source reference (such as the original filename and available date or location) in a separate host-only answer key.
4. Check every clue against the returned source information. A clue must not reveal the answer prematurely, depend on an unsupported guess, or expose private information. Skip a photo if it cannot support a fair clue; explain if fewer rounds are possible than requested.
5. Present the game in this format:
   - A short title and host instructions.
   - Numbered player rounds with clues labeled Hint 1, Hint 2, and Hint 3.
   - A separate answer key with the answer and source-photo reference for each round.
6. Provide the game in chat by default. If the user asks to save it, use an available NAS text/knowledge capability only after confirming the destination. Never overwrite an existing file without explicit confirmation.

# Completion and failure

Finish by stating how many usable rounds were created and listing any omitted rounds with a brief reason. If the selected album cannot be accessed, no photos are found, or the available results do not contain enough reliable context, say so plainly and ask the user to select another album or provide more context. Never fill gaps with invented details.

Do not modify, move, delete, or share original photos. Do not send album content to external services. Do not claim that a game was saved unless the save action succeeded.
