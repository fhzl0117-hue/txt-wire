# TXT Wire

An independent, unofficial English-language fan hub for TXT (Tomorrow X Together)/MOA — news translation, release reviews, official-only video curation, a live tour countdown, and a fan quiz, built to run on Google AdSense.

**Not affiliated with, endorsed by, or sponsored by Big Hit Music, HYBE, or the members of TXT.**

## What's in this repo

This is a single static page — `index.html` — with everything (HTML, CSS, JS) inlined. No build step, no dependencies, no backend. It's meant to be served as-is by GitHub Pages. This repo follows the same template as [Bangtan Wire](https://fhzl0117-hue.github.io/bangtan-wire/), [Blackpink Wire](https://fhzl0117-hue.github.io/blackpink-wire/), [Stray Kids Wire](https://fhzl0117-hue.github.io/stray-kids-wire/), [aespa Wire](https://fhzl0117-hue.github.io/aespa-wire/), [ENHYPEN Wire](https://fhzl0117-hue.github.io/enhypen-wire/), [SEVENTEEN Wire](https://fhzl0117-hue.github.io/seventeen-wire/), [TWICE Wire](https://fhzl0117-hue.github.io/twice-wire/), and [LE SSERAFIM Wire](https://fhzl0117-hue.github.io/lesserafim-wire/) — part of the "Wire" series, one dedicated site per artist.

The page is organized into six "desks," each mapped to a content pillar:

| Desk | Section id | What it does |
|---|---|---|
| 01 · News | `#news` | Translated & summarized news dispatches, each linking to its original source |
| 02 · Review | `#reviews` | Album / track reviews, text only |
| 03 · Screening Room | `#screening` | Official YouTube embeds only — never re-uploaded video |
| 04 · Signal | `#signal` | A live timer that counts down to confirmed future tour dates, or counts up ("time since") for past ones — auto-converted to the visitor's local timezone |
| 05 · Quiz | `#quiz` | A lightweight interactive quiz, no backend, no data collection |
| 06 · Market | `#market` | Links to official stores (affiliate links go here) |

## A note on accuracy: the STEAL THE WIND World Tour schedule

As of this build (August 2026), only the Seoul opening dates (November 13–15, 2026) for the STEAL THE WIND World Tour have been officially confirmed; Big Hit Music has stated the tour continues through Asia, North America, and Europe into June 2027, but individual city dates beyond Seoul had not been announced at time of writing. Do not fabricate city names or dates for the unannounced legs — wait for an official confirmation from Big Hit Music or a reputable outlet (Soompi, Korea Times, Korea JoongAng Daily) before adding new Signal Desk rows.

## manifest.json — K-Wire Network auto-discovery

This repo carries a `manifest.json` at its root so it's automatically picked up by [K-Wire Network](https://fhzl0117-hue.github.io/), the directory hub for the whole "Wire" series. No manual edit to the hub repo is needed — its page fetches this file on every visit and lists this site automatically.

## Updating content

Everything is plain HTML — open `index.html` in any editor and look for the section with the matching `id` (e.g. `<section ... id="news">`) to update copy. There's no CMS yet; each dispatch, review, or signal-desk date is a hand-edited block. See the comments inside the `<script>` tag at the bottom for how the quiz and countdown/elapsed timers work if you need to change their logic — the Signal desk timer auto-detects whether a `data-target` date is in the future (shows "time left") or the past (shows "time since"), so it works either way without further edits.

**Before adding new dates or news items,** verify the underlying facts against a real source and keep the "Read the original source" link pointing at it — that link is what keeps this page compliant with content policies (Google AdSense does not allow re-publishing copyrighted material, and this page's whole design is built around linking out and summarizing instead of reposting).

**Before adding any new YouTube embed,** verify it against the official channel using the oEmbed check: fetch `https://www.youtube.com/oembed?url=https://www.youtube.com/watch?v=<ID>&format=json` and confirm `author_name` matches HYBE LABELS (or the relevant member's own verified channel) — a search result titled "Official MV" is not proof by itself. During this site's initial build, a candidate "Beautiful Strangers" video from a channel styled "TXTi" (a lookalike of the real "TXT" credit) turned out to be a dead/nonexistent video entirely — the oEmbed check caught it before it was used.

## License / ownership

Internal company project. Not licensed for redistribution outside the team without checking with whoever owns this repo.
