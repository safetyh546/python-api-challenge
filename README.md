# Api Challenge Homework

## This homework required calling weather and google api's
Weather.py - randomly selects over 500 cities, calls open weather api to get weather in those cities and saves to dataframe<br />
It then plots Latitude against temp, humidity, wind and cloudiness to see if there is relationships between those variables<br />
Vacation.py - plots those 500+ cities on a heatmap with humidity as the weight<br />
It then narrows the 500+ down to smaller number of cities based on ideal weather conditions<br />
It then calls Google nearby search api to get a hotel in each city<br />
It then adds markers for these hotels to the heatmap created above<br />


## Temperature (F) vs. Latitude<br />
This plot analyzes relationship between Temperature and Latitude<br />
More than any of the other weather patterns,they appear correlated<br />
Specifically, temperature goes up as you approach latitude of 0<br />
Temperature gets smaller as you get farther away from latitude of 0<br />

## Humidity (%) vs. Latitude
This plot analyzes relationship between Humidity and Latitude<br />
Appears to be some relationship but not as strong as temparature<br />

## Cloudiness (%) vs. Latitude
This plot analyzes relationship between Cloudiness and Latitude<br />
The data is all over the place here, doesn't seem to follow a pattern<br />

## Wind Speed (mph) vs. Latitude
This plot analyzes relationship between Windspeed and Latitude<br />
Only observable trend is everyone seems to have wind in range of 0-30mph except for a couple outliers<br />
Doesn't appear that latitude relates to higher or lower wind speed<br />

# Linear Regression

## Northern/Southern Hemisphere - Temperature (F) vs. Latitude
Northern Hemisphere has a inverse regression, temp starting high and going down as you move away from lat = 0<br />
Southern Hemisphere has a postiive regression line, temp starting low and going up as you approach lat = 0<br />
Northern hemisphere r-value of .76 is close to 1 indicating significance as observed in plot above<br />
Southern hemisphere r-value of .39 is also significant<br />
## Northern/Southern Hemisphere - Humidity (%) vs. Latitude
Northern hemisphere r-value isn't as significant at r = .16<br />
Southern hemisphere r-value also is very small at r = .02<br />
in Northern - Some level of relationship seems to follow temp as humidity goes up as you get farther away from lat = 0<br />
## Northern/Southern Hemisphere - Cloudiness (%) vs. Latitude
r-value for both hemispheres is small<br />
Appears to be no real relationship between cloudiness and latitude<br />
## Northern/Southern Hemisphere - Wind Speed (mph) vs. Latitude
r-value for both hemispheres is small<br />
Appears to be no real relationship between wind speed and latitude<br />
