# Weather_Project

##  Project Description
Explored Weather Trends in Baltimore Maryland and compared trends globally. The data used was weather data from 1750 to 2013. The visual trends found in the data can be viewed in weatherwriteup.pdf file; simple-moving average was used.    

## Questions
1. Average Temperature for Baltimore Maryland
2. Average Temperature globally

## Requirements
1. Google Sheets
2. SQL database provided by @udacity

## SQL Query Used in Project
```sql
SELECT city_data.year, city_data.avg_temp
AS city_temp,
global_data.avg_temp
AS global_temp
FROM city_data
JOIN global_data
ON city_data.year = global_data.year
JOIN city_list
ON city_list.city = city_data.city
WHERE city_data.year = global_data.year
AND NOT city_data.avg_temp IS NULL
AND city_data.city = 'Baltimore';
```
