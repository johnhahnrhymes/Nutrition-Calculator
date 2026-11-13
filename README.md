# Larder

A single-file whole-foods nutrition tracker. No installation, no server, no internet connection required. Just one HTML file you open in any browser.

## What it does

Three tabs, nothing more:

1. **Calculator** — Search 309 whole foods, add any combination with amounts in grams, see the full nutrition breakdown (30 nutrients: 7 macros, 13 vitamins, 10 minerals). Hit **EAT** to log what you just ate to today's date.

2. **Recipes** — Save ingredient combinations as named recipes with serving counts. Edit them anytime. **EAT** on a recipe prompts for how many servings you ate and logs the right amount.

3. **Calendar** — View what you ate on any given day, or aggregate totals across a date range (last 7 days, last 30 days, or any custom range). Shows full nutrient breakdown and average kcal/day for ranges.

## Why

Most nutrition apps require accounts, push subscriptions, show ads, or sell your data. Larder does none of that. Your recipes and food log live only in your browser's local storage on your own device.

## Features

- **309 whole foods** across 22 categories: fruits, berries, citrus, melons, vegetables, leafy greens, mushrooms, root vegetables, alliums, grains, legumes, nuts, seeds, dairy, eggs, fish, shellfish, seaweed, herbs, spices, oils, sweeteners. No meat (poultry/beef/pork) — fish included.
- **30 nutrients per food** from USDA FoodData Central (public domain data).
- **FDA-compliant serving sizes** — every food uses the standard nutrition-label serving size as its default. An apple defaults to 154g (1 medium apple per FDA Appendix C), almonds default to 28g (1 oz / 23 almonds per FDA RACC), raw fish defaults to 113g (3 oz per FDA Appendix D). You can change any amount freely.
- **Works offline.** Once loaded, no internet connection needed.
- **Zero dependencies.** No React, no CDN, no npm, no build step. Pure vanilla HTML/CSS/JavaScript in a single file.
- **Export/Import.** Back up all your recipes and food log as JSON to move between devices.

## Try it live

If this repo has GitHub Pages enabled, you can use the app directly without downloading anything:

https://johnhahnrhymes.github.io/Nutrition-Calculator/

## Use it on your own device

### Windows / macOS / Linux

1. Download `Larder.html` from this repo (click the file, then click the download icon)
2. Double-click the file
3. It opens in your default browser

That's it.

### Android

1. Download `Larder.html` to your phone (email it to yourself, or use Google Drive)
2. Open it with Chrome
3. In Chrome, tap the three-dot menu → **Add to Home screen**

### iPhone

iOS is picky about local HTML files. The easiest way:

1. Send `Larder.html` to the phone (iMessage, email, or AirDrop) as `Larder.txt` to bypass iOS's HTML attachment blocker
2. Save it to the **Files** app
3. In Files, enable **Show All Extensions** (three-dot menu → View Options)
4. Rename `Larder.txt` to `Larder.html`
5. Long-press the file → Share → Safari
6. In Safari, tap Share → **Add to Home Screen**

Alternatively, use the live GitHub Pages URL above — simpler.

## Data

The raw nutrition data is in `data/`:

- `whole_foods_nutrition.csv` — CSV format
- `whole_foods_nutrition.json` — JSON format
- `whole_foods_nutrition.xlsx` — Excel format with color-coded columns

Each row has: food name, category, FDA serving size (grams), serving note (e.g. "1 medium apple"), then 30 nutrient values per 100g raw/edible portion.

**Data sources:**
- Nutrition values: [USDA FoodData Central](https://fdc.nal.usda.gov/) (public domain, CC0 1.0)
- Serving sizes: [FDA 21 CFR 101.12 RACC table](https://www.ecfr.gov/current/title-21/chapter-I/subchapter-B/part-101/subpart-A/section-101.12) and [FDA Appendices C & D](https://www.fda.gov/food/nutrition-food-labeling-and-critical-foods/nutrition-information-raw-fruits-vegetables-and-fish) (20 Most Frequently Consumed Raw Fruits/Vegetables/Fish)

## Privacy

Everything stays on your device. The app has no analytics, no telemetry, no network calls, no ads, no accounts. Your recipes and food log are stored in your browser's `localStorage` on each device separately.

If you clear your browser data, you lose your recipes. Use the **Export** button on the Recipes tab to save a backup.

## Known limitations

- Recipes and food log are **per-browser, per-device**. Build a recipe on your PC, and it won't appear on your phone. Use Export/Import to move data between devices.
- No automatic sync between devices.
- Local file storage can be path-sensitive on some browsers — keep `Larder.html` in a consistent location.
- The food database is baked in. No way to add your own foods in the current version.

## License

MIT — see [LICENSE](LICENSE).

The nutrition data from USDA FoodData Central is public domain (CC0 1.0).

## Contributing

This is a single-file app by design. If you want to propose changes, open an issue first to discuss what you have in mind. Pull requests are welcome, but keep the zero-dependencies rule: no CDN loads, no build step, no npm.
