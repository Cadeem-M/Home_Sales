# Home Sales

<p align="center">
<img src="Resources\Images\Screenshot 2024-08-06 154347.png" width="700px">
</p>

## Overview
I'll be using SparkSQL to determine key metrics about home sales data. Using Spark, I aim to create temporary views that can help analyze average house pricing giving specific parameters. After creating tables to analyze, I will try running a query on cached and partitioned data to compare run times. 


## Analysis and Results
To help analyze the data, I will consider the following:


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

4. What is the average price of a home per "view" rating having an average home price greater than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places. 

<p align="center">
<img src="Resources\Images\Screenshot 2024-08-06 154615.png" width="400px">
</p>

5. How is runtime impacted when the previous question is answered via an uncached table, a cached table and partitioning the data on the column "date_built"?

Uncached table
<p align="center">
<img src="Resources\Images\Screenshot 2024-08-06 154615.png" width="400px">
</p>

cached table:
<p align="center">
<img src="Resources\Images\Screenshot 2024-08-06 154704.png" width="400px">
</p>

partitioned data:
<p align="center">
<img src="Resources\Images\Screenshot 2024-08-06 154713.png" width="400px">
</p>



## Summary 
Upon reviewing the results of the queries:

1. The average price of a 4 bedroom house seemed to be increasing between 2019-2021 before decreasing in 2022.

2. The average price of 4 bedroom homes with 3 bathrooms that were built between 2010-2017, stayed rather consistent at around 292,000 with potential outlier years in 2015 (288,770) and 2013 (295,962).

3. The average price of homes built between 2010-2017 with three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet; seems to be declining over those years. There was a noticeable increase in 2013 but the years after show a downwards trend.

4. There doesn't seem to be any noticable trend between average pricing and View ratings as prices are sporadically increasing and decreasing as rating go down for the first 20 ratings. Perhaps more data is needed for a trend to form.

5. With the uncached table, the query ran in about 2.03 seconds. With the cached table, the query ran in about 0.92 seconds. With the partitioned data, the query ran in about 1.46 seconds. While the data set at hand is fairly small, we do see a performance difference in that the query using the cached table is substantially faster. 


## Credits/Helpful resources
For a refresher on how to manipulate dates in SQL, I recommend the video below as it was useful for me.

Baldwin,Cody. "Working with Dates (SQL) - EXTRACT, DATE_PART, DATE_TRUNC, DATEDIFF" YouTube, uploaded by Cody Baldwin, 3 Jan 2023, https://www.youtube.com/watch?v=XyZ9HwXoR7o