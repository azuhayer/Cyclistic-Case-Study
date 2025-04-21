```Title: Cyclistic Case Study``` <br>
```Author: Zuhayer Alvi``` <br>
```Date: 04-15-2025```

## Cyclistic Case Study Report

### ***Ask***
Ever since its launch in 2016, Cyclistic, a bike-sharing company, has grown to over 5,824 bicycles in a network of over 692 stations across the state of Chicago. So far, the company has relied on using various flexible pricing plans to attract customers: single-ride passes, full-day passes, and annual memberships. The company wants to increase its future growth by proposing the idea of converting existing casual riders to annual members, since annual memberships are deemed much more profitable for the company by the financial analytics team. 

As part of the Cyclistics analytics marketing team, my job will be to figure out how annual and casual riders use Cyclistic bikes differently and use those insights to design a strategy to encourage casual riders to become annual members. 

### ***Prepare***
The data that I will be utilizing to help the company come to a business decision are the ```Divvy_Trips_2019_Q1.csv``` and ```Divvy_Trips_2020_Q1.csv``` files. Both of these files have been made available through the Motivate International Inc. under this [license](https://divvybikes.com/data-license-agreement). These datasets give us information regarding the different types of customers and how they use Cyclistic bikes. With the help of various data analysis tools these public datasets will allow me to explore how annual members and casual riders use Cyclistic bikes differently. 

The datasets contain detailed information about ride start and end times, stations, user types, and trip durations—allowing for comparison between annual members and casual riders. Both files are stored in CSV (comma-separated values) format, making them suitable for analysis using Python and libraries such as pandas and NumPy. These tools will allow me to manipulate and explore the data effectively to identify usage trends between the two customer groups.

### ***Process***
I prepared and cleaned the data to ensure consistency and integrity before analysis.

- Loaded the datasets (```Divvy_Trips_2019_Q1.csv``` and ```Divvy_Trips_2020_Q1.csv```) into Python using pandas.
- Renamed columns in the 2019 dataset to match the 2020 schema for consistency.
- Converted datetime fields (started_at, ended_at) to proper datetime format.

Created new columns:
- ```ride_length``` (duration of each ride in seconds)
- ```day_of_week``` (weekday name derived from started_at)

Standardized values in the member_casual column (e.g., converted "Subscriber" to "member", "Customer" to "casual").

Filtered out:
- Rides starting at the internal station "HQ QR".
- Rides with negative durations.

After cleaning, I merged both datasets into a single DataFrame called ```all_trips_v2``` to perform the analysis.

### ***Analyze***
To understand how casual riders and members use Cyclistic bikes differently, I conducted a descriptive analysis on the ```ride_length``` and usage patterns:

Summary statistics for all users:
- Mean ride length: 1189.45 seconds 
- Median ride length: 539.0 seconds 
- Longest ride: 10632022.0 seconds
- Shortest ride: 1.0 second

Summary statistics between user types (member and casual):
- Mean ride length
  - casual: 5372.783874 seconds
  - member: 795.252339 seconds
- Median ride length
  - casual: 1393.0 seconds
  - member: 508.0 seconds
- Longest ride
  - casual: 10632022.0 seconds
  - member: 6096428.0 seconds
- Shortest ride
  - casual: 2.0 seconds
  - member: 1.0 second

Casual riders consistently take longer rides than members on average.

Weekly patterns:
- Members ride more consistently throughout the weekdays, especially for commuting.
- Casual riders show higher usage during weekends, suggesting more leisure-oriented behavior.

### ***Share***
To communicate my findings, I created the following visualizations:

1. Number of Rides by Rider Type and Day of the Week

![image](https://github.com/user-attachments/assets/2e5e3762-0f0c-4f96-a500-ae8f3c6b5a71)
Insight: Members ride more during weekdays; casual riders peak on weekends.

2. Average Ride Duration by Rider Type and Day of the Week

![image](https://github.com/user-attachments/assets/ae3f3388-85b7-4a0e-94b9-7c8cc402322e)
Insight: Casual riders consistently have longer rides, especially on weekends.

### ***Act***
Based on the analysis, I recommend the following:

1. Target weekend marketing campaigns toward casual riders, promoting the benefits of annual memberships for frequent leisure rides.

2. Introduce incentives for casual riders to subscribe—such as discounts on annual memberships for riders who take a certain number of trips per month.

3. Enhance the app experience by showing casual riders how much they could save or gain with a membership based on their ride history.

These insights will support the marketing team in crafting a focused strategy to convert casual users into annual members.


> [DISCLAIMER]
> Cyclistic is a fictional company, for the purposes of this case study all datasets used will enable me to showcase my data analysis skills and answer business related questions. 
