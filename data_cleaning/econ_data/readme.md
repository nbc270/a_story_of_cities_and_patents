The final output from these econ_data IPython Notebooks is to determine the number of creative class employees and establishments within cities of interest. Data originates from the US economic census. We use 5-year aggregates as they are more reliable than annual datasets. The years are 1997, 2002, 2007, and 2012. North American Industry Classification System (NAICS) codes and names are used to determine if a career of a person is within the creative class, per Dr. Richard Florida's definition. 

Follow the steps below for in order to succcessfully reproduce the data pipeline created. 

1) Run the _(year).ipynb first. These will perform the API call and format the data into a dataframe and will then be written out as a .csv file.

2) Run 2012_processing.ipynb. The reason this step is separate from the other cities is that a semi_processed and fully processed datasets are
produced. The semi processed is used in 2002_and_2007_pypsark_joins.ipynb which is the next step in order to semi process 2002 and 2007 datasets.
This is due to those years either not having both or just one of city names and NAICS titles. 

3) Run 2002_and_2007_pypsark_joins.ipynb next as explained above. 

4) Run the remaining (year)_processing.ipynb, which will produce final 5-year aggregates of creative class and establishment data. 
