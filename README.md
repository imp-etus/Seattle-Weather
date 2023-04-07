# DATA 3320, Project 1: Quantifying Rain in Seattle and St. Louis
## Overview
This project aims to answer the question: Does it rain more in Seattle, WA, or St. Louis, MO? 

Using daily precipitation measured in Seattle and St. Louis, this project aims to quantify the rain in each city between January 1, 2017 and December 31, 2022, and then present that using graphs and tables where necessary.
## Data
#### Sourcing
The NOAA Climate Data can be found [here](https://www.ncei.noaa.gov/cdo-web/search?datasetid=GHCND). Raw link: <https://www.ncei.noaa.gov/cdo-web/search?datasetid=GHCND>

More specifically, Seattle's data comes from the Boeing Field location, and St. Louis's data currently (as of 3/27) comes from the aggregate of all climate stations in St. Louis.

The specific data sets used were sourced from the Seattle U Data 3320 Github repository, which can be found [here](https://github.com/brian-fischer/DATA-3320/tree/main/weather). For both cities, the weather station at each respective airport was used.

#### Data Preparation
Data was prepared by normalizing date/time records. However, missing values were present in Seattle's dataset, especially in 2018. To replace them, we took the average precipitation for that day in all other years and replaced it. This preparation was done using the Colab notebook labeled "Data Preparation." Additionally, column names were cleaned up (for example, station names were dropped in favor of just using the city name & explaining what station was used in the notebook itself).

The clean data file is df_tidy.csv. However, monthly/yearly data was also included. `true_monthly_data.csv` refers to the fact that those values were taken as the aggregate of *all* years, rather than just a single year. All other csv's are pretty self-explanatory, I think.

