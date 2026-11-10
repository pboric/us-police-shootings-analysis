# Fatal Police Shootings in the United States

An analysis of The Washington Post's database of fatal police shootings in the US since 2015: trends over time,
who the victims are, where incidents happen, a statistical test of the trend and a simple forecast.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/pboric/us-police-shootings-analysis/blob/main/Police_Shootings_Analysis.ipynb)

## Key findings

- **California, Texas and Florida** have the most incidents.
- In absolute numbers most victims are white and most were armed with a gun; armed status differs between racial
  groups.
- The yearly totals rise, but a generalized additive model (GAM) of the monthly counts finds **no statistically
  significant trend** (p ≈ 0.4 for both spline terms).
- A Random Forest model forecasts about **1,150 fatal shootings for 2024**.

## What the notebook covers

1. Data cleaning and feature engineering (duplicates, data types, missing values, date features)
2. Descriptive statistics, temporal patterns by year and month
3. Demographics: age, race, gender, mental illness, armed status
4. Geography: incidents by state, with a map
5. Hypothesis test of the trend with a GAM
6. Forecast of the 2024 total with a Random Forest regressor

## Run it

The data is downloaded directly from The Washington Post's GitHub repository, so nothing needs to be prepared:

```bash
pip install -r requirements.txt
jupyter notebook Police_Shootings_Analysis.ipynb
```

## Limitations

The counts are not adjusted for population size. Comparing racial groups or states fairly would need rates per
person (for example per million residents), which can change the picture considerably.

## Data

[The Washington Post: Fatal Force database](https://github.com/washingtonpost/data-police-shootings) and US state
boundaries from the US Census Bureau.

## License

MIT
