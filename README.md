# Optimizing Bike Rental System in San Francisco

## Introduction:

San Francisco, a city embraced by enthusiasts of an active lifestyle, poses an ongoing challenge for bike rental service providers. At the heart of this dynamic environment, you work as an experienced data analyst for one of the leading bike rental companies in the region.

Your office is confronted with two key issues: convert casual riders into subscribers and managing the problem of malfunctioning bikes. Your primary goal is to provide valuable insights that will help the company expand its user base and optimize the operation of the bike fleet.

## Ask

### Business Task:

- How can we convert casual riders into subscribers?
- Optimize Bike Fleet Maintenance

### Analysis Questions

- How do annual members and casual riders use Cyclistic bikes differently?
- What is the Time Distribution of Bike Usage for Subscribers and Casual Customers?
- How Does Bike Usage Vary Across Different Hours of the Day for Subscribers and Casual Customers?
- What is the Weekly Pattern of Bike Rentals for Subscribers and Casual Customers?

## Prepare

### Data Source

[San Francisco Ford GoBike](https://console.cloud.google.com/marketplace/product/san-francisco-public-data/sf-bike-share?hl=pl&project=crack-node-393412) , managed by Motivate, provides the Bay Area’s bike share system. Bike share is a convenient, healthy, affordable, and fun form of transportation. It involves a fleet of specially designed bikes that are locked into a network of docking stations. Bikes can be unlocked from one station and returned to any other station in the system. People use bike share to commute to work or school, run errands, get to appointments, and more. The dataset contains trip data from 2013-2018, including start time, end time, start station, end station, and latitude/longitude for each station.

[Historical Hourly Weather Data 2012-2017](https://www.kaggle.com/datasets/selfishgene/historical-hourly-weather-data) dataset provides a comprehensive collection of weather-related information recorded at an hourly frequency. The dataset spans the years 2012 to 2017

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

Based on the bar chart, it can be observed that subscribers typically take shorter rides. The highest percentage of subscriber trips, over 20%, falls within the 5-10 minute duration category. On the other hand, customers seem to prefer longer rides. The highest percentage of customer trips falls within the 30-60 minute category.

![image](https://github.com/pjowsianka/San-Franciso-BikeTrips/assets/130370888/05b432cf-712c-4bb7-89ce-7a6b87b9ae20)

The line chart shows that the percentage distribution of trips at different hours of the day varies for subscribers and casual customers.
Subscribers have two peaks in bike usage, suggesting that they most often use the bikes for commuting to and from work or university.
On the other hand, casual customers most frequently use the bikes between 10:00 and 17:00. This might suggest that they use the service mainly during the day, perhaps for touring the city or other recreational activities.

![image](https://github.com/pjowsianka/San-Franciso-BikeTrips/assets/130370888/017b20d0-ade3-4f50-a4c2-88c98a4193d7)

![image](https://github.com/pjowsianka/San-Franciso-BikeTrips/assets/130370888/3d9a09f8-9530-4e16-9a24-0e15b7612eae)

The bar charts of Number of rentals for customers on each day of the week provide further support for the hypothesis that subscribers use bikes for commuting to work, as they exhibit lower usage on Saturdays and Sundays. Conversely, customers show higher bike usage on weekends, indicating a more leisure-oriented use, possibly for tourism or recreational activities.

![image](https://github.com/pjowsianka/San-Franciso-BikeTrips/assets/130370888/de287449-3fc1-47dc-b8e0-9ae6f663c7f8)

On the chart, we can see the top 10 most frequent bike rental locations for casual users. It could be beneficial to consider increased advertising in these areas, capitalizing on their popularity.


![image](https://github.com/pjowsianka/San-Franciso-BikeTrips/assets/130370888/08d598a1-1a5f-450e-a97f-4b716d03678f)

The Average Day Temperature and Trip Count by Month chart also suggests a correlation between the average temperature in San Francisco and the number of bike rentals. The visual representation indicates that variations in the average temperature coincide with fluctuations in the trip count, implying a potential relationship between weather conditions and bike rental patterns.


![image](https://github.com/pjowsianka/San-Franciso-BikeTrips/assets/130370888/ea10fb07-eb63-4238-ad60-3a1580e06f8a)

Through the analysis of the bar chart, we can observe that Sunday and Monday are the days when people generally use bicycles less frequently. This valuable insight can be instrumental in planning maintenance activities.

## Act


1. **Fleet Usage Optimization:**
    - *Recommendation:* Explore tailored subscription models to engage casual riders effectively. Consider introducing weekend-centric subscriptions at reduced rates, enticing users to utilize bikes on Saturdays and Sundays. This strategy aims to not only attract occasional riders but also maximize fleet utilization during low-traffic periods.

2. **User Engagement Strategies:**
    - *Recommendation:* Conduct surveys and establish a mailing list to gather insights on potential areas lacking bike stations. This proactive outreach aligns with the analysis showing that subscribers typically use bikes for commuting to work or university. Expanding bike stations strategically could tap into new user interest. Additionally, consider promoting services to employers and educational institutions as a means of encouraging bike commuting among employees and students.

3. **Advertising Campaign Timing:**
    - *Recommendation:* Initiate advertising campaigns earlier, leveraging the analysis that highlights August as the peak month for bike usage despite July being the warmest. By promoting cycling in advance, we aim to capture potential riders' attention and encourage the adoption of biking during the peak season.

4. **Strategic Advertising Presence:**
    - *Recommendation:* Increase the visibility of bikes through intensified advertising at stations frequented by our customer base. This targeted approach enhances brand recognition and encourages more individuals to opt for our services. Align advertising timing with observed behavioral patterns for maximum impact.

5. **Maintenance Optimization:**
    - *Recommendation:* Implement fleet bike maintenance optimization by focusing on low-traffic days, specifically Mondays and Sundays. This ensures efficient execution of regular maintenance procedures on these days.

6. **Additional Maintenance Enhancement:**
    - *Recommendation:* Integrate the provided SQL procedure into the maintenance routine. This procedure identifies heavily used bikes during the week, facilitating thorough inspections.

```SQL
CREATE PROCEDURE IF NOT EXISTS CheckHighUsageBikes()
BEGIN
    SELECT bike_number
    FROM bikeshare
    WHERE strftime('%Y-%w', start_date) = strftime('%Y-%w', 'now')
    GROUP BY bike_number
    HAVING COUNT(*) >= 100;
END;
```
By undertaking these actions, we aim to optimize fleet usage, engage users effectively, and enhance our bike-sharing service based on thorough analysis. The strategic expansion of bike stations aligns with the commuting habits of subscribers, potentially attracting new users. Simultaneously, promoting services to employers and educational institutions opens avenues for increased visibility and user adoption.
