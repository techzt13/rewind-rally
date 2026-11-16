# Clue rules

Linked from [SKILL.md](../SKILL.md).

## A hint is allowed only if

- It comes from a field the NAS returned for that exact photo (capture date, location label, scene or object label, or a person group the user already named).
- It does not reveal the answer before the last hint.
- It is understandable to the chosen player group.

## Always leave out

- Street addresses, home location, or coordinates more precise than a city or region.
- Photos that look like documents, IDs, receipts, or screenshots.
- Health, religion, or other sensitive personal details.
- Full names of children, and any person the user did not name.
- Anything on the user's exclusion list.

## Skip a photo when

- It has fewer than two usable fields.
- It is a near-duplicate (same date and place) of a photo already chosen.
- Its hints would be identical to another round's hints.

## Examples

| Source data | Good hint | Bad hint (why) |
| --- | --- | --- |
| Date: 2023-07-14 | "Hint 1: A summer day, two years ago." | "July 14, 2023" (too exact for Hint 1) |
| Location: Kyoto, Japan | "Hint 2: A city famous for temples." | "Grandma's favorite trip" (not in the data) |
| Labels: beach, cake | "Hint 3: Someone brought dessert to the sand." | "Leo's 8th birthday" (guessed event and name) |
