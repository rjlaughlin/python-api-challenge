# Python API Challenge: WeatherPy and VacationPy

## Overview

This project aims to analyze weather data and visualize trends across cities, providing insight into temperature, humidity, and other weather attributes. Additionally, these findings  are used to suggest potential vacation spots based on weather preferences. This project leverages APIs, JSON traversal, and data visualization tools to address key questions about weather and geography.

## Project Structure

This project is divided into two main parts:

### WeatherPy

In **WeatherPy**, weather data from over 500 cities is analyzed, examining relationships between various weather parameters and latitude. Using OpenWeatherMap's API, weather data is retrieved and visualizations are created to answer the question: "What is the weather like as we approach the equator?"

#### Key Tasks
- **Data Collection**: Gather weather data using the OpenWeatherMap API.
- **Visualization**: Generate scatter plots to analyze:
    - Latitude vs. Temperature
    - Latitude vs. Humidity
    - Latitude vs. Cloudiness
    - Latitude vs. Wind Speed
- **Linear Regression Analysis**: Separate data into Northern and Southern Hemispheres and compute linear regressions for each parameter against latitude.
- **Scatter Plot**: Latitude vs. Temperature, Humidity, Cloudiness, Wind Speed
- **Linear Regression**: Includes regression lines for each weather parameter in both hemispheres, R-squared values, and trend analysis.

### VacationPy

In **VacationPy**, ideal vacation locations are identified based on selected weather conditions. Using filtered weather data,Geoapify is used to find hotels near each location.

#### Key Tasks
- **Map Creation**: Display all cities on a map with point size based on humidity.
- **Data Filtering**: Filter cities by conditions like temperature, wind speed, and cloudiness to find vacation-friendly destinations.
- **Hotel Identification**: For each city, find the nearest hotel using the Geoapify API, and add hotel and country details to the map.
- **Humidity Map**: Cities displayed by humidity level.
- **Hotel Map**: Shows the name and country of hotels within selected cities.

## Files

- **WeatherPy.ipynb**: Notebook for Part 1, analyzing weather data.
- **VacationPy.ipynb**: Notebook for Part 2, identifying vacation spots.

## Setup and Dependencies

Before starting, ensure you have the following libraries installed:

```python
# Dependencies
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
import requests
import time
from datetime import date
import scipy.stats as st
from citipy import citipy  # For finding cities by geographic coordinates
```
You will also need API keys from:

OpenWeatherMap API: For weather data.

Geoapify API: For location-based services.

Please generate `api_keys.py` and place your API keys in the file as shown below:

```python
# api_keys.py
weather_api_key = "YOUR_OPENWEATHERMAP_API_KEY"
geoapify_key = "YOUR_GEOAPIFY_API_KEY"
```

## Running the Analysis
- Clone the repository and navigate to the project directory.
- Install dependencies as shown above.
- Run the Jupyter Notebook or Python script to generate the analysis and visualizations