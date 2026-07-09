# Verse & Advocate

A Bible verse finder for arguments. Describe your point in plain English — "forgiveness
is better than revenge", "pride comes before a fall" — and it ranks the verses that best
support it.

**Everything runs in the browser.** No backend, no API keys, no tracking. The full text
of each translation is bundled and searched locally in a few milliseconds.

## Features

- Plain-English argument search with a ~100-topic thesaurus that maps modern words to
  biblical vocabulary (revenge → vengeance, worry → "take no thought", money → mammon)
- Three translations: World English Bible (modern English), King James Version (1611),
  and Tyndale (1534, partial — Genesis–Deuteronomy, Jonah, and the New Testament)
- Old/New Testament filters, match highlighting, "why this matched" notes
- One-click copy with citation, and in-context preview of surrounding verses
- Ranking favors short, quotable verses; a stemmer tuned for archaic verb endings
  (loveth/lovest/loving all match "love") keeps the old translations searchable

## Run locally

Serve the folder over HTTP (needed for `fetch` of the text files):

```
python -m http.server 8642
```

then open http://localhost:8642.

## Texts

- **World English Bible** — public domain
- **King James Version** — public domain
- **Tyndale Bible (1534)** — public domain
- WEB and Tyndale files are [Bible SuperSearch](https://www.biblesupersearch.com/) modules;
  additional translations in that format can be added via the `TRANSLATIONS` map in
  `index.html` (mind the license of non-public-domain translations)

## Caveat

This is keyword/synonym search, not semantic understanding. It finds verses *about* your
topic but cannot tell which side of an argument a verse supports — read before you quote.
