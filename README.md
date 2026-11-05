# Netflix-Movies-TV-Shows---Data-Cleaning

**Tools:** Python (Pandas), Google Colab
**Dataset:** Netflix Movies and TV Shows (Kaggle), 8,807 rows × 12 columns

## Summary of changes
- Column names checked: already lowercase with underscores, no change needed
- Duplicates: checked full rows and `show_id`, found 0, so none removed
- Trimmed leading/trailing spaces in text columns (88 `date_added` values, 1 title)
- Fixed 3 rows where the runtime (e.g. "74 min") was stored in `rating`;
  moved it to `duration`
- Removed trailing commas from 5 `country` values
- Missing values: `director` (2,634), `cast` (825), `country` (831) filled with
  "Unknown"; `rating` (4) filled with "Not Rated"; 10 missing `date_added`
  left blank rather than guessed
- Converted `date_added` from text to a date, formatted dd-mm-yyyy;
  added `year_added` and `month_added`
- Split `duration` into numeric `duration_value` and `duration_unit` (min/Season)
- Final: 8,807 rows × 15 columns

## Files
- `netflix_titles.csv`: raw data
- `netflix_cleaned.csv`: cleaned data
- `netflix_data.ipynb`: code
