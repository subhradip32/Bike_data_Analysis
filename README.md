# Bike Data Analysis
This project is one of the most interesting project I have ever done till date. This project consists of understanding the microsoft SSH and the mysql database with it, And visualising the data using the opensource tool called PowerBI.
This helped me to understand the insights behind data and data visualisation with understanding the mysql queries and much more.

# About Project
As from the given figure its clear that I am using a bike selling dataset from the internet, in which there are three files seperated respectively. To generate optimum result I used the mysql query to help the data to combine and display it on the PowerBI.
I combined all the three files or dataset and generate a proper features out of the data.

```
with cte as (
select * from bike_share_yr_0 
union select * from bike_share_yr_1)

select dteday,season,a.yr,weekday,hr,rider_type,riders,price,COGS,
riders * price as reveue, 
riders * price - COGS as profit
from cte as a
left join cost_table as b
on a.yr =b.yr
```
The above query helped me to gather all the data over the three files and conatenate into a single one, which I used to build the dashboard below.

# Output
![Screenshot 2024-06-28 095504](https://github.com/subhradip32/Bike_data_Analysis/assets/83198378/18044d39-2077-4087-9442-8a6eaf01abee)
