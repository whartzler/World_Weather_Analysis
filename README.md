# World_Weather_Analysis

## Objective
We are working on the PlanMyTrip app to gather information to identify potential travel destinations and nearby hotels. 

### Weather DataBase
In this workbook we generated a list of 2,000 random latitudes and longitudes using Numpy.  With the generated latitudes and longitudes we ran an API request through [Open Weather Map](https://openweathermap.org/) to find the nearest city for each combination and stored the data into a list. Once the data was compiled into a los we created a DataFrame city_data, udpated the column order and saved the dataframe to a CSV.  This is the building block of our project.
[Weeather DataBase Notebook](https://github.com/whartzler/World_Weather_Analysis/blob/main/WeatherPy.ipynb)



### Vacation Search
Using the dataframe created in the WeatherDataBase notebook we used these randomly generated coordinates and created a new dataframe hotel_df based on the users imput of where they would like to travel based on min and max temperature.  We iterated through the dataframe hotel_df based on the longitude and latitude of each city to find the nearest hotel based on parameters set.  we cleaned and removed any NA Values to a new dataframe and saved to our folder as WeatherPy_vacation.  After the file was saved we plotted the data using gmaps.


### Vacation Itinerary
Using the csv created in Vacation Search titled 'WeatherPy_vacation' we used this data to create additional marker layers.  We identifies cities we want the customer might want to visit and created dataframes for each.  Using to_numpy() we retreived the latitude and longitude pairs as tuples for our map.  Once we identified the areas the customer might want to visit we plotted the information to show each waypoint on gmaps with the best way to get to each.  Finally we plotted each waypoint for the customer to see on a figure and saved the image.  
