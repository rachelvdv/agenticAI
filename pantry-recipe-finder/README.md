# Pantry — Recipe Finder

A single-page recipe finder. Add the ingredients you have on hand, optionally filter by cuisine, meal type, or diet, and it sorts a built-in recipe collection by how close each one is to ready. Everything runs client-side — no backend, no API keys, no data leaves the browser.

**[Live demo](#)** *(add your GitHub Pages link here once deployed)*

## Features

- Ingredient-based search with chip input and quick-add suggestions
- Filter by cuisine, meal type, and diet — usable alone or combined with ingredients
- Results ranked by ingredient match percentage
- Recipe detail view with a servings stepper that scales quantities live
- 30 built-in recipes across 12 cuisines
- Zero dependencies — one HTML file, no build step

## Running locally

Just open `index.html` in a browser. No install, no server required.

```bash
git clone https://github.com/YOUR_USERNAME/pantry-recipe-finder.git
cd pantry-recipe-finder
open index.html   # or double-click the file
```

## Deploying to GitHub Pages

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`.
4. Pick the `main` branch and `/ (root)` folder, then save.
5. Your app will be live at `https://YOUR_USERNAME.github.io/pantry-recipe-finder/` within a minute or two.

## Adding your own recipes

Recipe data lives in the `RECIPES` array near the top of the `<script>` block in `index.html`. Each entry follows this shape:

```js
{
  id: 31,
  title: "Recipe Name",
  cuisine: "Italian",
  meal: "Dinner",              // Breakfast | Lunch | Dinner | Snack
  diet: ["vegetarian"],        // any tags you want to filter by
  time: 30,                    // minutes
  servings: 4,
  difficulty: "Easy",
  ingredients: [["garlic", "2 cloves"], ["pasta", "400 g"]],
  steps: ["Step one.", "Step two."]
}
```

New cuisines, meal types, and diet tags are picked up automatically by the filter dropdowns — no other code changes needed.

## Tech

Plain HTML, CSS, and JavaScript. No framework, no package manager, no build step.

## License

MIT — see [LICENSE](LICENSE).
