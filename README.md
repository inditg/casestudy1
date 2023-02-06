# Case Study 1: How does a Bike-share navigate speedy success

<a> <img src="./images/ciclystics.png" width=150/></a>

# Author: Indira Torres Gimenez

## Scenario:
I'm a junior data analyst working in the marketing analyst team at Cyclistic, a bike-share company in Chicago.
In 2016, Cyclistic launched a successful bike-share offering. Since then, the program has grown to a fleet of 5,824 bicycles that are geotracked and locked into a network of 692 stations across Chicago. The bikes can be unlocked from one station and returned to any other station in the system anytime. 
Pricing plans: 
1.	single-ride passes 
2.	full-day passes
3.	annual memberships.
Customers who purchase single-ride or full-day passes are referred to as casual riders. 
Customers who purchase annual memberships are Cyclistic members.
The company’s future success depends on maximizing the number of annual memberships. 

## Business task: 
Design marketing strategies aimed at converting casual riders into annual members.
My task: Answer one of the three questions that will help to setup the future marketing program - How do annual members and casual riders use Cyclistic bikes differently?

## Data source: 
The data used on the analysis is the previous 12 months of Cyclistic trip data available on this link <a href="https://divvy-tripdata.s3.amazonaws.com/index.html"><img src="./images/datasource.png" width=200/></a>


The data has been made available by motivate International Inc. under this license <a href="https://ride.divvybikes.com/data-license-agreement"><img src="./images/licenseagreement.png" width=200/></a>

This is a public data and is not missing important information.
The data is not biased, the data is cleaned, given by the certificate course
The data sources we are using ROCCC:
* Reliable and Original: This is public data containing accurate and complete information about Cyclistic's historical bike rides
* Comprehensive and Current: There is not missing important information needed to understand the differences between Cyclistic ‘s members and Cyclistic ‘s casual riders. The data is current and relevant.
* Cited: The data source is public by Cyclistic and the City of Chicago.

## Data cleaning and manipulation
Because the data source files provided is extensive, I used the data related with the first quarter of 2020, 2021 and 2022. This data can show how the program performed in the first quarter of the year for three consecutive years.
I downloaded the zip files related with the years that I would like to analyze and unziped. I store those file on OneDrive and my local computer on a folder. I saved copies in .CSV and .XLS to have copy of the original data.

### Microsoft Excel
1.	Splitted the started_at and ended_at columns into two different columns to separate date and time, the new columns are called started_at_date, started_at_time, ended_at_date, ended_at_time  
 <a><img src="./images/spplitedcolumns.png" width=1000/></a>

2.	Changed format of the date and time columns
* Home > Format > Format Cells 
* Format > Cells > Date > yyyy-mm-dd for started_at_date and ended_at_date columns
* Format > Cells > Time > h:mm:ss for started_at_time and ended_at_time  columns
3.	Created a column called ride_length 
* Calculated the length of each ride by subtracting the column started_at from the column ended_at (example: =D2-C2)
* Formatted as TIME
* Home > Format > Format Cells > Time > HH:MM:SS (37:30:55)
4.	Created a column called day_of_week
* Calculated the day of the week that each ride started using the WEEKDAY command (example: =WEEKDAY(C2,1))
* Formatted as a NUMBER with no decimals
* Format > Cells > Number (no decimals) > 1,2,3,4,5,6,7

Note: 1 = Sunday and 7 = Saturday

After making these updates, I saved each .XLS file as a new .CSV file.
Analysis
Because the datasets provided are too large, I move to BigQuery to use SQL for data analysis.

## Analysis #1: 
Explore your data and look for maximum rife length in the Q1 of each year. 

<a><img src="./images/dataQ1.png" width=1000/></a>

<a><img src="./images/maxride.png" width=200/></a>  
The maximum ride length on the first quarter of each year is very similar, almost the same.

## Analysis #2:
To help the team to identify the areas where we should focus the campaign to increment the number of members I calculated the number of casual riders peer station and I identify the top 20 of the stations with more riders.

<a><img src="./images/analysis2.png" width=1000/></a>
<a><img src="./images/analysis2.png" width=600/></a>

## Analysis #3: 
Some stations are repeated in the list of stations with the most casual riders in Q1 of the last three years. 
We can see here the top 10 of the stations with more casual riders and some of the stations are included on the list for 3 years. So, we can focus the attention on this places to convert these numbers of riders in members.

<a><img src="./images/analysis3.png" width=1000/></a>
 
For example: These two stations are on the top15 list of more casual riders on the Q1 of the last three years

<a><img src="./images/analysis31.png" width=1000/></a>

 







