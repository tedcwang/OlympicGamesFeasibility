Olympic Games Feasibility Analysis
----------------------------------
Served as the final project for GEOG 215 Introduction to Spatial Data Science

Spring 2020

### Introduction
Ever since its inception in Ancient Greece and its revival at the dawn of the 20th century, the Olypmic Games have attracted millions of people to witness the miracle of human sport and athleticism. Every two years, thousands of atheletes from around the world travel to one central hub to participate in the Olympic Games, seen by many as the ultimate measure of prestige and test of skill and talent. Every Olympic Games alternates between winter and summer, each with their own unique events and special body of atheletes who come to compete with the best across the globe.

Accordingly, there is a process by which cities from various countries can place their bids to host the next Olympic Games. In recent years, however, and especially compared to its origins more than a century ago, the Olympic Games and their host cities face ever more arduous challenges. Cities have spent anywhere from millions to billions of dollars organizing, planning, and hosting the games; there are many cases where hosting the games eventually financially ruined the city. Financial costs, infrastructure, and climate conditions threaten the future of the games and the feasibility of certain locations in hosting them. How do changing temperatures affect the ability of cities in hosting the Olympics? Which locations should be avoided or sought after in hosting either the summer or winter Olympics? Can we visualize a history of spending by each country on hosting the Olympic Games?

Using R to conduct a temperature anomaly analysis and geospatial study using historical temperature data, as well as a brief statistical financial analysis, this report analyzes the history of previous Olympic Games venues and the feasibility of future locations for future games.

### Data
This file contains data sets recording monthly mean air temperatures from the years 1900 to 2017 interpolated to a 0.5 by 0.5 degree grid resolution; data is provided by the Global (Land) Precipitation and Temperature initiative by the National Center for Atmospheric Research by Willmott and Matsuura at the University of Delaware:
http://climate.geog.udel.edu/~climate/html_pages/Global2017/air_temp_2017.tar.gz

This is historical climate data provided by WorldClim v2, showing the average and maximum temperatures around the globe based on a 10 minute (~340 square kilometer) scale. Each .zip file contains 12 .tif files, each representing a month of the year (01 is January, 02 is February, etc.): http://biogeo.ucdavis.edu/data/worldclim/v2.1/base/wc2.1_10m_tavg.zip (average temperature)
http://biogeo.ucdavis.edu/data/worldclim/v2.1/base/wc2.1_10m_tmax.zip (maximum temperature)

This data set is provided by the National Centers for Environmental Information as part of the National Oceanic and Atmospheric Administration (NOAA). This particular climate data set is a global time series query specifying a timescale of 1 month (July, when most summer Olympic Games start), starting in 1880 to 2020 (last recorded year is 2019). The resulting data set offers the year of record and the value of the temperature anomaly recorded:
https://www.ncdc.noaa.gov/cag/global/time-series/globe/land/1/7/1880-2020/data.csv

This data set was taken from data.world; it contains the financial costs of each Olympic Games from 1960 to 2016 in billions of dollars, as well as the location, season (summer or winter), and number of atheletes that attended. These data figures are from one source and may differ from other reported data:
https://query.data.world/s/c64ruj3biyf5wpefrp7e724fd7o35e

This country shapefile provides the necessary geospatial data, projected as a WGS84 reference system, needed to add location to the financial data above:
https://opendata.arcgis.com/datasets/a21fdb46d23e4ef896f31475217cbb08_1.zip

### Downloading and viewing the .rmd file
Click on the .rmd link to view the file in GitHub UI. There you should be able to see a button "Raw". Right click "Raw" and choose "Save Link As", then save where ever you wish on your device. You should be able to view the file now.

Alternatively, if you already have R and RStudio installed, you can simply open the .rmd file there.
