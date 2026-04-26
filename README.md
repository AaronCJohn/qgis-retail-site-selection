# Chicago Retail Site Opportunity Analysis (QGIS)

![Final Map](final_layout.png)

## Overview

Spatial analysis identifying underserved retail markets in Chicago by cross-referencing U.S. Census tract population density with Starbucks locations as the primary competitor. The goal: surface high-population areas with low Starbucks saturation as candidate sites for new retail placement.

---

## Methodology

- **Data acquisition:** Loaded U.S. Census tract shapefiles with population attributes and geocoded Starbucks locations as point features
- **Competitor coverage modeling:** Generated 0.5-mile buffers around each Starbucks to approximate serviceable trade areas
- **Spatial join:** Joined buffer coverage to Census tracts to calculate the number of Starbucks locations within or overlapping each tract
- **Underserved area identification:** Filtered for tracts in the top quartile for population density and bottom quartile for Starbucks buffer coverage
- **Output:** Choropleth map symbolizing opportunity score by tract, with Starbucks sites overlaid for spatial context

---

## Results

The analysis identified **14 Census tracts** across the South and West sides of Chicago meeting both the high-population and low-coverage thresholds. These tracts collectively represent an estimated **~180,000 residents** within areas where Starbucks density falls below the citywide median.

---

## Key Insight

Starbucks coverage in Chicago is heavily concentrated in the Loop, River North, and Lincoln Park corridors. The South Shore, Auburn Gresham, and Humboldt Park neighborhoods show the strongest combination of population density and Starbucks gap, making them the highest-priority candidates for new retail site evaluation.

---

## Tools

| Tool | Purpose |
|---|---|
| QGIS 3.x | Spatial joins, buffer analysis, map rendering |
| U.S. Census Bureau TIGER/Line | Census tract boundaries and population data |
| Starbucks Store Locator (public) | Competitor location dataset |
| EPSG:26916 (NAD83 / UTM Zone 16N) | Projected CRS for accurate buffer distances |
