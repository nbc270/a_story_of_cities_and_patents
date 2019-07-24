For regulation data, we are using three data which are from Federal Funding, Small Business Innovation Research (SBIR) Program and Empowerment Zone (EZ) Program. Federal funding and SBIR program data are available from websites mentioned below and need to be downloaded manually as there isn't appropriate api call to get our desired data. EZ data are obtained from a report* by General Accounting Office and has been cleaned into a downloadable csv file called EZs.csv in 'Empowerment_Zone' folder. There is also a csv file called EZ_raw.csv which has exact same 

Follow the steps below to produce desired data:

1. Federal Funding Data

a) In 'Federal_Funding' folder, create a folder named 'byCity'

b) Go to: https://www.usaspending.gov/#/download_center/custom_award_data \
For each year (2001 to 2012), fill in options as following and click download:

Award level: Prime Awards \
Award types: Select All \
Agency: All \
Recipient location: Country: United States \
                    State: All \
Date type: Action Date \
Date range: Start Date: 01/01/year \
            End Date: 12/31/year \
File format: CSV

c) For each year: unzip the downloaded folder and change its name to year (eg. 2001)

d) Run the ff_toCity.ipynb by changing the year variable (recommend one year at each time instead of running in a loop to avoid kernel crashing since each year’s data is over 5G)

e) Run the ff_cleaning_data.ipynb

2. SBIR Data

a) In 'SBIR' folder, create three folders named byYear, byCity and clean_SBIR

b) Go to: https://www.sbir.gov/sbirsearch/award/all \
For each year (2001 to 2014): \
i) Create a folder with year (eg. 2001) as the name inside the 'SBIR' folder\
ii) Go to the link above and Select desired year (eg. 2001) on the left \
iii) Click on Download then Click on all .XLS to download csvs into the folder named with the year (eg.2001)

c) Run the sbir_toCity.ipynb

d) Run the SBIR_cleaning.ipynb

* EZ Report link: https://www.gao.gov/new.items/d04306.pdf (Appendix II)