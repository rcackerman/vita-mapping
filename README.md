# VITA Mapping Project

## Repository Purpose
This repository will contain all data used for the VITA mapping project. It also contains Jupyter Notebooks that cover cleaning and prepping.

The final product will be mapped on Tableau Public (link tbd).

## Installation

#### Census API key
First, set up your [Census API key](https://api.census.gov/data/key_signup.html). We use the API key by saving it to a `.env` file.

Save the .env-sample file to .env.
```
mv .env-sample .env
```

Then replace the text `<YOUR API KEY HERE>` in .env-sample with the API key you just got from [the Census](https://api.census.gov/data/key_signup.html).

#### Python & Jupyter setup
You'll need [python 3](https://www.python.org/) and [Jupyter](https://jupyter.org/) installed.

With homebrew:
```
brew install python jupyter
```

Then install the necessary python libraries:

```
pip install python-dotenv
pip install pandas
pip install geopandas Fiona folium Shapely rtree
pip install census
``` 

## Data Sources

* 2019 zip code tabulation area shapefiles: https://www.census.gov/geographies/mapping-files/time-series/geo/cartographic-boundary.2019.html
* 2019 ACS detailed datasets: https://data.census.gov/cedsci/all?t=Income%20%28Households,%20Families,%20Individuals%29&g=0100000US%248600000&d=ACS%205-Year%20Estimates%20Detailed%20Tables
  * Specifically, "Household Income in the Past 12 Months (In 2020 Inflation-Adjusted Dollars)" 5 year estimate data tables at the 5-digit zip code tabulation area (ZCTA) summary level (https://data.census.gov/cedsci/table?t=Income%20%28Households,%20Families,%20Individuals%29%3AIncome%20and%20Earnings&g=0100000US%248600000&d=ACS%205-Year%20Estimates%20Detailed%20Tables&tid=ACSDT5Y2020.B19001).

* 2018 ZCTA shapefiles: https://www.census.gov/geographies/mapping-files/time-series/geo/carto-boundary-file.html
* 2018 ACS household income: https://data.census.gov/cedsci/table?t=Income%20%28Households,%20Families,%20Individuals%29%3AIncome%20and%20Earnings&g=0100000US%248600000&d=ACS%205-Year%20Estimates%20Detailed%20Tables&tid=ACSDT5Y2018.B19001
