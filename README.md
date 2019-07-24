This repository is dedicated to storing reproducible notebooks that may provide data collection, analysis, and visualization towards identifying how cities can invest in their economic future. Our we use publicly avialable patent data as our target variable and our indepdent features include regulatory, socio-economic, and demographic data. In the end we determined that if a city were currently trying to become an innovation hub, they should try to investment in higher education, work on policy to promote immigration, and create environments that promote entrepreneurial endeavors. We determined this by running the regression analyses found on the main page of this repo. 

Below are the insturctions for conducting the analysis reproducibly. 

1) Run all data_cleaning notebooks first, starting with each data type, and then aggreating over the years of interest. 

2) Once data has been aggregated you may create regression files and run all analyses
    - a) Run Create_regression_file.ipynb to create a file that is clean and standardized and ready for regressions
    - b) Run random_forest_regressions.ipynb to uns random forest regressions to get the feature importance charts for each year and score
Runs logistic regression for each year to calculate AUC scores
    - c) Run Random_forest_over_time.ipynb to run the a random forest regression for each year and plots each features trends over 2001-2012
    - d) Run Logistic_regressions.ipynb to run a logistic regressions for each year to get nice plots with All cities, Bottom cities, and Top cities.

3) Create files for visual
    - a) Run Read_geojson.ipynb to Creates all relevant files for d3 map visualization
    - b) Run the code this [gist](https://gist.github.com/rohuniyer/d36f9823189e0183fd3a41ba79ffb0e3) to create an interactive visual that will allow you to compare two cities innovation producing features over time
    - c) Run the code this [gist](https://gist.github.com/tingyuc3/6f878fe46e588feab3e5d3796519e36a) to create an interactive visual that provides spatial context to this analysis
