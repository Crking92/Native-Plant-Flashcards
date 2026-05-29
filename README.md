# Native Plant Flashcards - Spreadsheet Build

Generated from `Master_Plant_Database(9).xlsx`.

## What is included

- `daily_flashcard.html` — browser flashcard app.
- `Data/master_plants.json` — JSON plant dataset.
- `Data/daily_data.js` — JavaScript plant dataset used by the app.
- `Data/flashcard_summary.csv` — flat review table for checking cards.
- `Data/duplicates_merged.csv` — duplicate scientific names merged into one card.
- `conversion_audit.json` — build summary and caveats.

## Build summary

- Spreadsheet rows with scientific names: 317
- Unique flashcards created: 315
- Duplicate scientific names merged: 2
- Cards with photos: 313
- Cards with larval-host notes: 107

## Notes

The source spreadsheet did not have a dedicated plant family column. Where possible, family names were copied from your previously uploaded flashcard JSON if the scientific name already existed there. Otherwise, the card says `Not listed in spreadsheet`.

To use on GitHub Pages, keep the `Data` folder name capitalized because the HTML loads `Data/daily_data.js`.

## Interface update

This build includes a cleaner start screen:

- Batch study buttons in groups of 50 plants.
- Search results stay hidden until a search term is typed.
- The full plant list no longer displays immediately on page load.


## Photo behavior

This build uses live iNaturalist photo lookup when each card opens. The original Lady Bird Johnson Wildflower Center image links remain in the dataset as backup links, but the front of the card now prefers iNaturalist photos because those are more reliable on GitHub Pages and allow multiple photos per plant.

Photo credits and observation links are shown on each image. Study progress is saved locally in the browser using localStorage.
