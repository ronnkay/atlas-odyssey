# Atlas Odyssey 🌍

An original browser-based geography game inspired by the broad idea of map-based geography challenges. Atlas Odyssey is not affiliated with Farflung or its creators.

## Play locally

1. Download or clone this repository.
2. Open `index.html` in a modern browser. (For best results, use a local development server because browsers may restrict network-loaded data from `file://`.)
3. Or deploy the repository with GitHub Pages.

### Run a local server

With Python installed, run this from the project folder:

```bash
python -m http.server 8000
```

Then visit http://localhost:8000.

## Publish with GitHub Pages

1. Create a new GitHub repository named `atlas-odyssey`.
2. Upload `index.html`, `styles.css`, `app.js`, and this README to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select `main` and `/ (root)`, then save.
6. Wait for GitHub Pages to publish your site.

## Features

- Five-round daily expedition with a date-seeded prompt selection.
- Unlimited practice mode.
- Clickable country outlines and country search.
- Five rarity tiers and distance scoring.
- End-of-game scorecard and copy-to-clipboard sharing.
- Local browser statistics using `localStorage`.
- Responsive layout for desktop and mobile.

## Data and dependencies

- [Leaflet](https://leafletjs.com/) for the interactive map.
- Country boundary GeoJSON from [datasets/geo-countries](https://github.com/datasets/geo-countries), loaded at runtime.
- Google Fonts for typography.

The map and its country boundaries require an internet connection. Game progress and statistics are stored locally in the browser; there is no account or server-side database.

## Customizing prompts

Edit the `PROMPTS` array near the top of `app.js`. Each prompt has:

- `id`: unique prompt identifier.
- `title`: the clue shown to the player.
- `note`: a short clarification.
- `answers`: object mapping exact GeoJSON country names to a score (`40`, `55`, `70`, `85`, or `100`).

Keep answer names consistent with the GeoJSON country names for map matching and scoring.

## License

The Atlas Odyssey source code is provided under the MIT License. External libraries and geographic data remain subject to their own licenses and terms.
