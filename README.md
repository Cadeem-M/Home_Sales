# Home Sales

<p align="center">
<img src="Resources\Images\Screenshot 2024-08-06 154347.png" width="700px">
</p>

## Overview
I'll be using SparkSQL to determine key metrics about home sales data. Using Spark, I aim to create temporary views that can help analyze average house pricing giving specific parameters. After creating tables to analyze, I will try running a query on cached and partitioned data to compare run times. 


## Analysis and Results
To help analyze the data, I will answer the 4 questions below:


1. What is the average price for a four-bedroom house sold for each year? 

<p align="center">
<img src="Resources\Images\Screenshot 2024-08-06 154504.png" width="500px">
</p>

2. What is the average price of a home for each year the home was built, that has three bedrooms and three bathrooms? 

<p align="center">
<img src="Resources\Images\Screenshot 2024-08-06 154520.png" width="500px">
</p>

3. What is the average price of a home for each year the home was built, that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? 

<p align="center">
<img src="Resources\Images\Screenshot 2024-08-06 154541.png" width="500px">
</p>

4. What is the average price of a home per "view" rating having an average home price greater than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places. (I will also include the run time for this query.)

<p align="center">
<img src="Resources\Images\Screenshot 2024-08-06 154615.png" width="500px">
</p>

## Summary 
https://www.youtube.com/watch?v=XyZ9HwXoR7o - Working with Dates (SQL) - EXTRACT, DATE_PART, DATE_TRUNC, DATEDIFF