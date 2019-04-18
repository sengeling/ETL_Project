# ETL_Project

# TEAM MEMBERS
C. Marshall Doig,
Stephanie Engeling,
Ashley McGee

# PROPOSAL
We will be pulling Formula 1 race data for the American Grand Prix and weather data for the race date for each Grand Prix city.

# DATA SOURCES
1. Original Data source 1 (FORMAT: CSV): Formula 1 race data - Formula 1 Race Data from 1950 to 2017 https://www.kaggle.com/cjgdev/formula-1-race-data-19502017

Four csvs used:

a. circuits.csv: Contains a list of every formula 1 circuit, including name, location and geographic data.
b. drivers.csv: Contains a list of every Formula 1 driver, including full name, dob, and nationality.
c. races.csv: Details of every race, including year, date, time, circuit and round
d. results.csv: The results for each driver in each race

2. Original Data source 2 (FORMAT: CSV): Weather data is the Local Climatologcial Data from NOAA.gov - https://www.ncdc.noaa.gov/data-access/land-based-station-data/land-based-datasets/quality-controlled-local-climatological-data-qclcd

Two csvs with valid data requested from NOAA:

a. austin_weather.csv: Hourly, daily, and monthly weather observations from the Austin-Bergstrom International Airport station between Nov. 1, 2012, and Oct. 31, 2018.
b. indy_weather.csv: Hourly, daily, and monthly weather observations from the Indianapolis International Airport station between Sept. 1, 2000, and June 30, 2007.

#FORMATTING NEEDED
1. Race data:

a. Get rid of unknown or uncommon races and only pull US races from circuits.csv and races.csv and then merge them
b. Merge drivers and results csvs on driver id
c. combine the two merged dataframes, drop unwanted columns, rename poorly named columns

2. Weather data:

a. Keep only rows that contained daily weather observation data (not hourly or monthly).
b. Drop all columns that contain all null values, and then drop columns deemed unnecessary.
c. Rename remaining columns, clean 'date' column so only month, date, and year remain.
d. Loop through list of race dates and keep only rows of daily weather data that match those dates.

# DATABASE TYPE

SQL Database (Relational) - joined by date

