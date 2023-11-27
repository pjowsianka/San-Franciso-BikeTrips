# Optimizing Bike Rental System in San Francisco

## Introduction:

San Francisco, a city embraced by enthusiasts of an active lifestyle, poses an ongoing challenge for bike rental service providers. At the heart of this dynamic environment, you work as an experienced data analyst for one of the leading bike rental companies in the region.

Your office is confronted with two key issues: convert casual riders into subscribers and managing the problem of malfunctioning bikes. Your primary goal is to provide valuable insights that will help the company expand its user base and optimize the operation of the bike fleet.

## Ask

### Business Task:

- How can we convert casual riders into subscribers?
- When should we maintain bicycles, and which bicycles should we focus on to minimize issues with them?

### Analysis Questions

- How do annual members and casual riders use Cyclistic bikes differently?


## Prepare

### Data Source

San Francisco Ford GoBike , managed by Motivate, provides the Bay Area’s bike share system. Bike share is a convenient, healthy, affordable, and fun form of transportation. It involves a fleet of specially designed bikes that are locked into a network of docking stations. Bikes can be unlocked from one station and returned to any other station in the system. People use bike share to commute to work or school, run errands, get to appointments, and more. The dataset contains trip data from 2013-2018, including start time, end time, start station, end station, and latitude/longitude for each station.

Historical Hourly Weather Data 2012-2017

### Data Organization

The first table contains San Francisco Ford GoBike bike rental data, such as the rental ID, rental start and end times, start and end station names, start and end station IDs, bike number, user postal code, bike subscription type, starting and ending station latitude and longitude, user birth year, user gender, and information about the bike-sharing program for all participants.

The second and third tables contain hourly weather history data from 2012-2017. The second table contains the date and time, city name, and temperature in Kelvin in the column with the city name. The third table contains the date and time, city name, and a brief description of the weather, such as “sunny,” in the column with the city name.

## Process

The data cleaning and preparation process involved trimming the dataset to include only records within a full year timeframe, specifically from January 1, 2014, to December 30, 2017, as the original dataset spanned from August 29, 2013, to April 30, 2018. Subsequently, the focus was narrowed down to extracting weather data exclusively related to San Francisco. Finally, a view was created by merging these two tables and converting Kelvin temperatures to Celsius.

## Analyze and Share

The data is stored appropriately and is now prepared for analysis. I queried multiple relevant tables for the analysis and visualized them in Python by Matplotlib.
The analysis question is: How do annual members and casual riders use Cyclistic bikes differently?

First of all, member and casual riders are compared by the time of using a bike.

![image](https://github.com/pjowsianka/San-Franciso-BikeTrips/assets/130370888/cd756bfb-0632-4dc4-a2d1-cf7dffeb2f74)



