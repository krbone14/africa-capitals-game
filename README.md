# 🌍 Capitals of Africa · Les Capitales d'Afrique

An educational geography game: drag (or tap) each of the 54 African capitals — or countries — onto the right spot of the map. Built as a single self-contained web page, playable on desktop and mobile.

**🎮 Play online:** https://krbone14.github.io/africa-capitals-game/

## Features

- **Three game modes** — place the capitals, the countries, or the flags
- **5 regions + whole-continent challenge** (all 54 countries)
- **Bilingual** — French / English, switchable at any time
- **Fun facts & flags** — every correct answer shows the country's flag and one of several rotating anecdotes
- **Mobile friendly** — tap a label then tap the map, pinch to zoom, responsive layout
- **Installable PWA** — add it to your home screen and play fully offline (flags included)
- **Score, stars & best-score tracking** (saved locally in the browser)
- **Sound effects** and confetti 🎉

## Run locally

No build step needed — it's a static page. Serve the folder with any static server, e.g.:

```bash
npx serve .
# or
python -m http.server 8000
```

then open `http://localhost:8000`. Opening `index.html` directly from disk also works in most browsers.

## Project structure

```
index.html            # the whole game: UI template + game logic
manifest.json         # PWA manifest (install to home screen)
sw.js                 # service worker: offline cache (app shell + all 54 flags)
icons/                # PWA / home-screen icons
assets/
  africa-geo.js       # window.AFRICA_GEO — SVG paths of the 54 countries + capital coordinates
  dc-runtime.js       # declarative-component runtime (generated, do not edit)
  asset_*.woff2       # Fredoka & Nunito fonts (self-hosted)
```

Country flags come from [flagcdn.com](https://flagcdn.com) and are pre-cached by the service worker for offline play.

## Contributing

Ideas, translations to new languages, and additional country anecdotes are welcome — the data lives in `index.html` (`C`, `XF` and `T` objects).

## License

MIT

---

## 🇫🇷 En français

Un jeu de géographie éducatif : glisse (ou touche) chacune des 54 capitales — ou chacun des pays — d'Afrique au bon endroit sur la carte.

- **Deux modes** : capitales ou pays
- **5 régions + le défi du continent entier**
- **Bilingue** français / anglais
- **Drapeaux et anecdotes** variées à chaque bonne réponse
- **Jouable sur téléphone** : touche une étiquette puis la carte, zoom par pincement
- **Score, étoiles et meilleurs scores** sauvegardés dans le navigateur
