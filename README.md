# MoMA Nationality Analysis: Representation Across Decades

This project analyzes acquisition patterns in the Museum of Modern Art’s collection to explore how artist nationalities are represented over time. Through data cleaning, decade-based grouping, percentage calculations, and treemap visualizations, this analysis highlights trends, biases, and gaps in curatorial practice from the 1930s to the 2020s.

---

## Project Overview

The dataset contains acquisition data from the Museum of Modern Art, including artist nationality and date of acquisition. After cleaning and enriching the data, artworks were grouped by decade and analyzed for nationality representation.

Key research goals include:
- Identifying **which nationalities dominate** MoMA's acquisitions
- Uncovering **trends in growth or decline** over time
- Highlighting **underrepresented regions**
- Offering **visual insights** via treemaps and trend charts

---

## Function Library

### `clean_nationality_column(df)`
Cleans the `'Nationality'` column by replacing empty or malformed entries and correcting common inconsistencies.

### `assign_decade(date)`
Assigns a decade string (e.g., `'1930s'`) based on the year of a given acquisition date.

### `group_by_decade(df)`
Groups the DataFrame into a dictionary of decade-based subsets using `assign_decade`.

### `extract_nationalities(series)`
Parses and extracts clean nationality strings from parenthetical list entries.

### `calculate_percentages(counts)`
Converts a Counter of nationality counts into percentage values.

### `generate_treemap(data, title)`
Displays a treemap visualization from a DataFrame containing `Nationality` and `Percentage` columns.

### `top_nationalities(data, n)`
Returns a DataFrame with the top `n` nationalities by percentage.

### `calculate_trend_analysis(data)`
Generates a pivot table of nationalities across decades and calculates their growth over time.

### `save_to_excel(filename, dataframes)`
Saves multiple DataFrames to an Excel workbook, with one sheet per DataFrame.

---

## Data Cleaning Notes

Before upload, the dataset was partially cleaned in Excel:
- Thousands of missing or malformed nationalities were researched and filled manually
- Collective or corporate entities were assigned nationality by origin
- Acquisition entries before 1930 were excluded for data quality and consistency

Final cleanup and formatting was done in Google Colab using `pandas`.

---

## Analysis Process

### Grouping by Decade
Acquisition dates were parsed and converted to `datetime`, then grouped by decade (1930s–2020s) for longitudinal analysis.

### Calculating Nationality Representation
Nationalities were extracted, counted, and converted into percentages for each decade. “Nationality Unknown” entries were excluded.

### Trend Analysis
All decades were merged into a single DataFrame to calculate the growth (or decline) of each nationality across time.

---

## Visualizations

### Treemaps
- Generated in Colab using `squarify`
- Enhanced in Illustrator and Canva
- Custom styles applied by decade (e.g., muted palettes for older decades, vibrant for recent ones)
- Inset maps added to improve legibility for low-frequency nationalities

### Final Visuals
- All visualizations re-styled for clarity and storytelling
- Icons, typography, and custom color palettes reinforce the evolving themes

---

## Key Findings

- **Dominance of American Art:** Grew from ~54% in the 1930s to over 61% in the 2020s
- **Decline of European Dominance:** Nationalities like German, French, and British showed decreasing share
- **Emerging Latin American Presence:** Modest growth for Cuban, Brazilian, and Chilean artists
- **Underrepresentation:** African, Oceanian, Southeast Asian, and Central Asian nationalities remain largely absent

---

## Opportunities for Change

This project provides a visual and data-driven map for more equitable acquisition strategies. The data points toward historical biases but also highlights regions that are beginning to emerge — offering a foundation for inclusive curatorial planning.

---

## Data + Notebooks

- `Artworks 2.csv` — Cleaned and analyzed in Colab
- All decades exported as CSVs and compiled into `artworks_combined.xlsx`
- Python functions and logic available in accompanying `.ipynb`

---

## How to Reproduce

1. Clone the repo  
2. Upload your dataset to Colab  
3. Run the notebook cell-by-cell to clean, group, and visualize  
4. Final visuals can be enhanced in Illustrator or Canva as desired

---

## License

This project is for educational and research purposes. Data is derived from the public MoMA Artworks dataset.
