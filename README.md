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

#### Running the code
The repo is split into 2 workflows, based mainly on which map the data are being used for. First, for [VITA Sites vs eligibility](https://public.tableau.com/views/VITAsites/Dashboard2?:language=en-US&:display_count=n&:origin=viz_share_link), we use the files:
* `1. get ACS data.ipynb`* and
* `VITA sites matched to county.ipynb`.

The other workflow is for [VITA sites vs MFT use]():

1. `1. get ACS data.ipynb`*
2. `2. MFT Processing.ipynb`
3. `3. Merging MFT to ACS relational file.ipynb`
4.  and `4. MFT at the county level.ipynb`

\* You only need to run this file once, even if you're rebuilding both maps.

## Data sources used

* 2019 county shapefiles: https://www.census.gov/geographies/mapping-files/time-series/geo/cartographic-boundary.2019.html
* 2019 ACS detailed datasets: https://www.census.gov/data/developers/data-sets/acs-5year.2019.html
  * Specifically, "Household Income in the Past 12 Months (In 2020 Inflation-Adjusted Dollars)" [(group B19001)](https://api.census.gov/data/2019/acs/acs5/groups/B19001.html) 5 year estimate data tables at the county summary level.

## Data sources for further work
While doing this project, we also found [income tax return data from the IRS](https://www.irs.gov/statistics/soi-tax-stats-individual-income-tax-return-form-1040-statistics), including VITA returns.

* 
