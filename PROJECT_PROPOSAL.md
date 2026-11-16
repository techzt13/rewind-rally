# Rewind Rally

## Project summary

Rewind Rally turns an authorized UGREEN NAS photo album into a host-ready guessing game for friends, families, clubs, and classmates. Players hear progressive clues about a moment, make a guess, and then see the original photo revealed by the host.

## Inspiration

People collect photos from trips, parties, school years, and everyday life, but usually revisit them by scrolling alone. Rewind Rally makes those shared memories a reason to play together.

## How it works

The host selects one album, the audience/tone, and a round count. The Skill uses available NAS album and photo capabilities to gather source-backed details, then creates clue rounds and a separate answer key that references the original images. It skips a photo when the available information cannot support a fair clue. Original media remains untouched; the game is returned in chat unless the user confirms a save location.

## What makes it NAS-native

The game is generated from media already stored in the user's private NAS library. It does not require uploading photos to an external game service, and each answer can be checked against its source photo.

## Challenges and learning goals

The central challenge is making clues surprising without inventing personal details. The Skill must distinguish evidence returned by NAS capabilities from guesses, skip weak material, and keep the answer key separate from player-facing hints. Testing should measure how often a host can verify each clue and whether players can answer before the final hint.

## Current status

The included Markdown Skill package is an initial proposal-stage version. It has not yet been tested in a UGREEN AI NAS environment; finalist testing should verify the supported photo-search workflow, clue quality, and save behavior.

## Demo plan

Use an authorized demo album. Show the album selection, one round with progressively revealed clues, and the answer key linking back to the original photo. Do not display private photos without permission.
