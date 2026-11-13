# Black Mesa redlines

What is known about the Black Mesa Research Facility as the games and mods build it: what people say about each map, what the
games' signs, announcements and other sources say about the facility's places and its days, and which mods count. Generated answers (what bmab's detectors
find) live here too once reviewed, and anyone can correct any entry. These files are made and edited with bmab, the tool that
reads the games; git history says who changed what and when.

Nothing from the games is in here: no geometry, pictures, sounds or text, except short transcriptions of text in a picture (a
sign) that a tool can't read itself. Everything else refers to the game files by path, sha256 and position, or to a web page by
its address, with the day it was read.

## Layout

| Path | One entry is |
|---|---|
| `maps/<game>/<map>.jsonl` | a claim about one map of one game: something at a spot (a connector, a fake door, a fake out, an area that isn't the facility, a part, an opening, a level change, a same place), or about the whole map (its place, whether it shows the facility before or after the incident, the file version the claims are about, which kinds of claim a person has checked) |
| `sources.jsonl` | a game, expansion, mod, outside work or website: title, kind (game, work or site), edition (original or remake), tier (how much it counts, 1 first) and, for a mod once judged, its verdict (admitted or reserve with its rank, rejected with why, pending, duplicate, reference) and the evidence the verdict rests on |
| `evidence/<source>.jsonl` | something a source says, never interpreted, with its tier: in the source's files (its kind: sign, announcement, caption, screen text, voice line, manual page...; file, sha256, where in the file, the maps that show or play it), or a web page (its kind: store page, wiki page, review, article, community post; address, the day it was read, and whether it was read first-hand or only through a search engine's summary) |
| `facts.jsonl` | one statement about places, from a fixed list of relations (in, near, above, leads to, tram stop, is, length...), naming the evidence that says it |
| `places.jsonl` | a place of the facility and its type (region, facility, sector, area, complex, level, room, transit, thing, elsewhere) |
| `events.jsonl` | something that happens at the facility on a day: the date as month and day (no source gives the year), the time and place when known, naming the evidence that says it |
| `rules/<name>.json` | a decided modelling rule with its numbers (`surface`: maps with open sky reach the surface) |

Every file holds one JSON object per line, sorted, so that edits to different things merge cleanly. Entries refer to each other
by id. A map is named by its game (a source's id) and its name in that game.

## Licence

[CC BY-SA 4.0](LICENSE).
