# python-api-challenge
## WeatherPy & VacationPy

# Weather Analysis
This project consists of two Python notebooks, WeatherPy and VacationPy, that analyze weather and map data across the world and visualize weather patterns vs latitude and identify ideal vacation spots.

# Dependencies
The scripts require the following Python libraries:

matplotlib
pandas
numpy
requests
time
scipy.stats
citipy
hvplot.pandas
holoviews
You also need to import your OpenWeatherMap and Geoapify API keys from a file named api_keys.py.  

# WeatherPy
The WeatherPy notebook generates a list of 1500 random latitude and longitude combinations, and uses the citipy library to find the nearest city to those coordinates. The script then makes a request to the OpenWeatherMap API for each city, and retrieves data about the city’s weather. The script outputs the weather data for each city into a pandas DataFrame, which is then saved as a CSV file in the output_data directory. The script also creates scatter plots for the following relationships:

City Latitude vs. Temperature
City Latitude vs. Humidity
City Latitude vs. Cloudiness
City Latitude vs. Wind Speed

# VacationPy
The VacationPy notebook loads the CSV file created by WeatherPy into a pandas DataFrame. The script then uses the Geoapify API to search for hotels within a 10,000 meter radius of each city. The script logs the search results and adds the hotel name to the DataFrame. If no hotel is found, the script sets the hotel name as “No hotel found”. The script uses the hvplot library to create a map plot of the cities, with the size of each point corresponding to the city’s humidity. The script also filters the DataFrame to remove all rows that show "No Hotel Found" and creates a map plot of the first 50 hotels found in the previous step.