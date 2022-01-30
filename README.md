# Python-API-challenge
Write a script to visualize 500 cities globally with varying distances from the equator. Use the weather data to help plan vacations.

# WeatherPy
## Random city gather
- Create a for loop to id cities, utilizing a random latitude and longitude generation using random.uniform
- Use a counter to ensure the minimum list of 500 unique cities is obtained with no duplicates

## Pull APIs with city inforamtion
- Create empty lists
- Create two counters:
    - Set
    - City
    - Initiate an if statement that will count the number of cities and the number of sets to log the cities obtained
    - Reset the ctiy counter each time a set of 50 is completed

## Convert API obtained data to float
- Since API data obtained is as string, must convert to float
- Create csv with utf-8 encoding
- Describe the data set

## Filter dataframe
- Remove cities with humidity > 100
- Test filtering by printing out the df with cities that have humidity > 100 and counting
- Remove records with null values and double check no values with > 100% humidity

## Create dataframes for souther and northern hemisphere plotting
- Use loc to filter dataframes
- Test creation of dataframes using min(latitude) for northern and max(latitude) for southern hemispheres. Northern hemisphere will not have latitude < 0 degrees. Southern hemisphere won't have latitude >= 0 degrees.

## Plots and commentary
- Create csv with commentary
- Create for loop that will create plots and add commentary after each plot
- Save image to png for each image

# VacationPy
## Read in csv from WeatherPy
- use pandas read csv
- remove null values
- count number of duplicates removed to verify will have number needed

## Create dataframes for heatmap
- Create df with lat, lon and humidity (for weight of heatmap)
- use gmap.figure to generate heatmap

## Desirable city list
- Set requirements, using loc, to id ideal vacation spots based on weather
- Pull on Google Place API to id hotels within 5000 meters of desirable city
- Use try/except to prevent missing data from causing error to break
- Print out hotel list to ensure < 10 hotels identified to meet project requirements

## Final heatmap
- Add markers for hotel to heatmap
- Using info_box_content allow user to click on each marker to see:
    - Hotel name
    - Hotel city
    - Hotel country

