# What's the Weather Like?

## Background

I gathered dataset from OpenWeather to answer a fundamental question: "What's the weather like as we approach the equator?" by analyzing the coorelation between latitude and weather conditions. Then, created a heatmap with hotel names of the cities from the dataset by using Google Map and Places API.


### Part I: WeatherPy

In this section, I create a Python script to visualize the weather of 610 cities of varying distance from the equator. By using a [simple Python library](https://pypi.python.org/pypi/citipy), the [OpenWeatherMap API](https://openweathermap.org/api) to gather the representative model of weather across cities.

First, a series of scatter plots with analysis to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude


Second, compute the linear regression for each relationship. This time, separate the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

A summary analysis is concluded base on the plots.

### Part II: VacationPy

Base on the weather data from part I to plan future vacations. Use Jupyter-gmaps and the Google Places API for this part of the assignment.


* Create a heat map that displays the humidity for every city from Part I, as the image file heatmap.png in Images folder.

* Narrow down the DataFrame to find the ideal weather condition:

  * A max temperature lower than 80 degrees but higher than 70.

  * Wind speed less than 10 mph.

  * Lower than 5% cloudiness.

* Use Google Places API to find the first hotel for each city located within 5,000 meters of these cities.

* Plot the hotels on top of the humidity heatmap, with each pin containing the **Hotel Name**, **City**, and **Country**, as in the image file heatmapwithmarker.png in Images folder.


### Summary Analysis:

* In this dataset, there are more cities in northern hemisphere then southern, which is a result of the fact 90% of the human population and more landmass in the northern hemisphere.
* Overall,the temperature is higher when latitude approching the equator,and vice versa.(fig:lat vs. temp plot)
* The cities around the equator have high humidity and cloudiness mostly.(fig:lat vs. humidity and lat vs. cloudiness plot), this could be the reason why the temperature around equotor isn't the highest.
* When comparing the northern and southern hemisphere, northern has more extreme temperature (30-100F) and lower wind speed than southern (40-90F), this is possibly because of there are more ocean to adjust the temperature and less land (or mountains) to lower the wind speed in southern hemisphere. A further study bases on the land, ocean papulation percentage in northern and southern hemisphere to compare the weather conditions/ factors will help to understand and the weather difference between them.

