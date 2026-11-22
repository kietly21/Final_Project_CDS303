## 1. Integrating Primary and Supplementary Datasets
Our main dataset is the 2025 DC crime incident file. We integrated it with two supplementary datasets: Alcohol License Business Locations & Metro Station Entrances.

| Dataset | Provider/Publisher | Unit | Role |
|---|---|---|---|
| Crime Incidents in 2025 | DC Metropolitan Police Department | 1 reported incident | Time and offense mix of crime |
| Alcohol License Business Locations | Alcoholic Beverage and Cannabis Administration | 1 license | Nightlife measures |
| DC Metro Station Entrances | Washington Metropolitan Area Transit Authority | 1 station entrance |Transport access |
| Census Tracts in 2020 | DC Open Data |1 tract polygon | Geography for the combinations, 2020 population, housing units, and land area |
|---|---|---|---|

### 2. What each row represents
In the integrated dataset, one row represents one 2020 census tract in Washington, D.C. There are 206 rows, and every variable defines that tract's: timing and combination of its 2025 crime, the number of alcohol licenses and Metro entrances within it, and its population, ACS demographics, and land area. 

### 3. Identifiers that connect the datasets
The datasets are connected through the location where:

- Each license, incident, Metro entrance is allocated to a tract by spatial join against the 2020 tract polygons.
- The tract's GEOID (census identifier: 11001 + 6-digit tract code) is the merge key. The ACS table is combined with the same GEOID and the tract code is the last 6 digits of FIPS code.
- GEOID is utilized only to merge and name rows.
  







   Create a table with all the census tracts and create new variables, like: Share of Violent crimes, Theft, Property damage, or etc.
   Can also include temporal variables, like: Times: Evening, Midnight, Daytime.
   Create an Excel file that includes all ~200+ census tracts.
New supplementary dataset: https://opendata.dc.gov/datasets/DCGIS::alcohol-license-business-locations/about

Second supplementary dataset: https://catalog.data.gov/dataset/metro-station-entrances-in-dc
- This connects to our dataset


  
## 2. Collect Data
   ACS

## 3. Spatial Join
