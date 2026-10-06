# Democracy and Economic Development

## Research Question

How is economic development associated with liberal democracy across five prominent countries?

## Overview

This project examines the relationship between economic development and liberal democracy across the United States, China, Germany, Brazil, and South Africa between 2000 and 2024.

The analysis combines the **V-Dem Liberal Democracy Index** with **GDP per capita** data from the World Bank to examine whether countries with higher levels of economic development also tend to have higher levels of liberal democracy.

## Countries and Period

- United States
- China
- Germany
- Brazil
- South Africa
- 2000–2024

## Data

### Liberal Democracy

Source: **Varieties of Democracy (V-Dem), Core Dataset Version 16**

Variable:
- `v2x_libdem` — Liberal Democracy Index

### Economic Development

Source: **World Bank**

Indicator:
- GDP per capita (current US$)

The datasets were matched by country and year, producing **125 country-year observations**.

## Method

The analysis was conducted in Python using pandas and matplotlib.

The main steps were:

1. Filter the datasets to the five selected countries and 2000–2024.
2. Harmonize country names.
3. Merge the V-Dem and World Bank data by country and year.
4. Calculate the Pearson correlation between GDP per capita and liberal democracy.
5. Calculate country-level averages.
6. Calculate within-country correlations.
7. Visualize the relationships using time-series and scatter plots.

## Key Findings

Across all 125 country-year observations, GDP per capita and liberal democracy had a moderate positive correlation:

**r = 0.548**

At the country-average level, the correlation was:

**r = 0.603**

However, the within-country relationships were highly heterogeneous:

| Country | Within-country correlation |
|---|---:|
| Brazil | 0.081 |
| China | -0.919 |
| Germany | -0.643 |
| South Africa | 0.390 |
| United States | -0.411 |

The positive cross-national association therefore does not consistently appear within individual countries over time.

China provides a particularly important contrast: substantial economic development occurred alongside persistently low levels of liberal democracy. Brazil showed almost no linear relationship between the two variables, while South Africa showed a moderate positive association.

## Interpretation

The findings suggest that richer countries in this five-country sample tended, on average, to have higher levels of liberal democracy.

However, economic development does not appear to have a uniform relationship with democratization within countries.

The results should therefore **not** be interpreted as evidence that economic development causes democracy. Political institutions, historical trajectories, political crises, and domestic and international factors may also shape democratic development.

## Limitations

- The analysis covers only five countries.
- The country-average correlation is based on only five observations.
- Correlation does not establish causation.
- The analysis does not control for other factors that may influence democracy.
- Within-country correlations capture linear associations rather than causal effects.
- GDP per capita is measured in current US dollars and is not adjusted for inflation.

## Conclusion

Economic development and liberal democracy are positively associated across the countries examined, but the relationship is neither uniform nor deterministic.

The contrast between the cross-national and within-country results demonstrates why economic development alone cannot explain differences in democratic trajectories.

## Files

- `Week_2_Democracy_and_Development.ipynb` — Python analysis and visualizations
- `week2_democracy_development.csv` — merged country-year dataset
- `week2_final_results.csv` — country-level results
- `week2_within_country_correlations.csv` — within-country correlations

## Data Sources

- Varieties of Democracy (V-Dem), Core Dataset Version 16
- World Bank, GDP per capita (current US$)
