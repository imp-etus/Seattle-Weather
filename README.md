# DATA 3320, Project 1: Quantifying Rain in Seattle and St. Louis
## Description
### Overview / Methods
This project aims to answer the question: Does it rain more in Seattle, WA, or St. Louis, MO? 

Using daily precipitation measured in Seattle and St. Louis, this project aims to quantify the rain in each city between January 1, 2017 and December 31, 2022, and then present that using graphs and tables where necessary. Basic bar charts were used to quantify rain, but more details are available in the Data Analysis section.

### Conclusion

In general, it rains more in St. Louis than Seattle. Seattle has more rainy winters, while St. Louis has more rain in spring and summer. For more details, see the Conclusion pdf.

## Requirements

Google Colab was used to generate the .ipynb files (notebooks). 

## Data
### Sourcing
The NOAA Climate Data can be found [here](https://www.ncei.noaa.gov/cdo-web/search?datasetid=GHCND). Raw link: <https://www.ncei.noaa.gov/cdo-web/search?datasetid=GHCND>

More specifically, Seattle's data comes from the Boeing Field location, and St. Louis's data currently (as of 3/27) comes from the aggregate of all climate stations in St. Louis.

The specific data sets used were sourced from the Seattle U Data 3320 Github repository, which can be found [here](https://github.com/brian-fischer/DATA-3320/tree/main/weather). For both cities, the weather station at each respective airport was used.

### Data Preparation
Data was prepared by normalizing date/time records. However, missing values were present in Seattle's dataset, especially in 2018. To replace them, we took the average precipitation for that day in all other years and replaced it. This preparation was done using the Colab notebook labeled "Data Preparation." Additionally, column names were cleaned up (for example, station names were dropped in favor of just using the city name & explaining what station was used in the notebook itself).

The clean data file is df_tidy.csv. However, monthly/yearly data was also included. `true_monthly_data.csv` refers to the fact that those values were taken as the aggregate of *all* years, rather than just a single year. All other csv's are pretty self-explanatory, I think.

The data preparation notebook is `Data Preparation.ipynb`.

## Analysis

The clean data files were taken & then converted to graph format with precipitation plotted versus time. The file 'Data Analysis.ipynb' does this preparation. df_monthly and df_yearly were converted directly, but df_yearly was grouped by year to let the graph look like a timeline rather than comparing months to each other, as that would provide a more human-readable result. df_monthly_max was used to contrast with the averages, as "which ity gets the heaviest rain day" can also be relevant.

The analysis notebook is `Data Analysis.ipynb`.

## Authors

Evelyn McCarty (bmccarty (at) seattleu.edu)

## License

MIT License

Copyright (c) 2023 evelyn mccarty

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
