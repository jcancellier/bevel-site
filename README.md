# Bevel site

The GitHub Pages source for Bevel: Ricochet Puzzle (App Store id 6836523701): the game page,
privacy policy, terms of use and support. Plain HTML and one stylesheet: no scripts (but the challenge page's own), trackers,
cookies or external fonts. Colours come from the game's theme (`games/game1/src/ui/theme.ts`).

- `index.html`: the game page, with the App Store link.
- `privacy.html`, `terms.html`, `support.html`.
- `c/index.html`: a friend's challenge (`c/?room=5&shots=2`), sent from the game's share card: the
  room and the shots to beat, Open in Bevel (`bevel://challenge?…`) and the App Store. One small
  inline script reads the query (checked as the app checks it, set as text only) and picks the
  language from the browser, in the game's 11; no network calls, no redirect.
  `c/og.png` is its link preview, drawn by `games/game1/scripts/make-challenge-og.ts`.
- `style.css`, `icon.png` (the app icon, 256 px).

## Placeholders to fill before publishing

- `joshua.cancellier@icloud.com`: the contact address (every page; also in `mailto:` links).
- `TelemetryDeck`: the analytics service's name (privacy.html).
- `California`: the US state whose law governs the terms (terms.html).


## Keep the privacy policy true

It describes what the app does. Update it (and the date at the top) when the app changes:
real ads going live, the analytics transport being switched on, Game Center going live, or any new
SDK or network request.
