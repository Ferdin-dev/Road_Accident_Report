# Road Accident Report

## Project Overview

This project aims to analyze road accident data to identify patterns and trends that can be used to improve road safety and reduce the number of casualties. The project uses a variety of data analysis techniques, including descriptive statistics, and data visualization.

![Dashboard 1](https://github.com/Ferdin-dev/Road_Accident_Report/assets/55439765/97384871-5131-4bfe-925d-532bb3b7ca78)


## Table of Contents
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Collection](#data-collection)
- [Data Preparation](#data-preparation)
- [Data Analysis](#data-analysis)
- [Findings](#findings)
- [Recommendations](#recommendations)
- [Screenshots](#screenshots)
- [Demo](#demo)

## Data Sources

Road Accident Data: The primary dataset used for this analysis is the “Road Accident.csv” file, containing detailed information about the company employee.

## Tools
- Excel – Data cleaning
- SQL Server – Data Analysis
- Power BI – Creating reports

## Data Collection

The data includes information on the following variables:

- Date and time of accident
- Location of accident
- Type of accident
- Type of vehicles involved
- Number of casualties
- Weather conditions
- Road conditions

## Data Preparation

Once the data was collected, it was necessary to clean and prepare it for analysis. This involved removing any duplicate or incomplete records, and converting the data into a format that could be easily analyzed using statistical software.

## Data Analysis

Once the data was prepared, a variety of data analysis techniques were used to identify patterns and trends. This included:

- Descriptive statistics: This was used to summarize the data and provide insights into the overall characteristics of road accidents.
- Data visualization: This was used to create charts and graphs that illustrate the patterns and trends identified in the data.


## Exploratory Data Analysis
EDA involved exploring the sales data to answer key questions, such as:
- Are there any specific days or times when accidents are more likely to occur?
- Where do most accidents occur? (e.g., urban vs. rural, specific districts)
- What types of vehicles are most commonly involved in accidents?

## Data Analysis
Include some interesting code/features worked with:

### Power BI

#### All Measures

Total Accident
```
Accident Count = COUNTROWS(Road_Accident_Data)
```
Total Accident with police
```
Accidents with Police = COUNTROWS(FILTER(Road_Accident_Data,Road_Accident_Data[Police_Force] <> BLANK()))
```
Average Casualties
```
Average Casualties = AVERAGE(Road_Accident_Data[Number_of_Casualties])
```
Average Vehicles
```
Average Vehicles = AVERAGE(Road_Accident_Data[Number_of_Vehicles])
```
Percentage Accident with police
```
Percentage Accidents with Police = DIVIDE([Accidents with Police], [Accident Count])
```
### SQL

Total Accident
```
select count(Accident_Date) as total_accident
from Road_Accident_Data
```
Total accident by day of week
```
select day_of_week, count(Accident_Date) as total_accident
from Road_Accident_Data
group by Day_of_Week
order by total_accident desc
```
Day of week with highest accident
```
select top 1 day_of_week
from Road_Accident_Data
group by Day_of_Week
order by count(Accident_Date) desc
```
Total accident by accident severity
```
select Accident_Severity, count(Accident_Date) as total_accident
from Road_Accident_Data
group by Accident_Severity
order by total_accident desc
```
Top 5 vehicle type involved in Accident
```
select top 5 Vehicle_Type, count(Accident_Date) as total_accident
from Road_Accident_Data
group by Vehicle_Type
order by total_accident desc
```

## Findings

The analysis of the road accident data revealed a number of key findings, including:
- The most common type of vehicle involved in accident is a car.
- The most common time of day for road accidents is during the evening.
- The most common location for road accidents is on urban roads.
- The most common day the accident occurs is on Friday.

## Recommendations

Based on the findings of the data analysis, a number of recommendations were made for improving road safety, including:
- Increasing enforcement of traffic laws, such as speed limits and drunk driving laws.
- Improving road infrastructure, such as traffic lights and sidewalks.
- Raising awareness of road safety issues among drivers and pedestrians.

## Screenshots


![Dashboard 3](https://github.com/Ferdin-dev/Road_Accident_Report/assets/55439765/7a6f29ae-1f8e-4446-af4d-2596135a9090)


![Dashboard 2](https://github.com/Ferdin-dev/Road_Accident_Report/assets/55439765/728f1a07-0a15-4fa6-82ad-c244c406d968)


![Dashboard 1](https://github.com/Ferdin-dev/Road_Accident_Report/assets/55439765/9f2c63c4-a568-4f0b-8276-82686960c1b7)

## Demo

https://github.com/Ferdin-dev/Road_Accident_Report/assets/55439765/02464856-12ac-49e4-b791-c9649c456be0

