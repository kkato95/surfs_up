# The SurfsUp Challenge
## Overview of the Analysis
The purpose of this analysis was to determine the tempurature trends of June and Decemeber in Oahu to find if the surf and ice cream shop with have sustainable business all year around. We are breaking up the analysis into two seperate deliverables. The first deliverable is to determine the tempurature summary statistic for June and the second is the tempurature summary statistics for December. 

## Results

Our analysis requires us to import our dependenices, which include: numpy, pandas, and sqlalchemy.

We had to create the engine variable using create_engine(), reflected an existing database and tables, saved the references to each table, and created the link from Python to DB.

![engine_hawaii](https://user-images.githubusercontent.com/99375741/166160262-3c2e2e24-23e6-4daf-905f-5ac5004d2845.png)


### Deliverable 1: Determine Summary Stistic for June

For deliverable 1, we are determining the summary statistics for the tempurature in June. To achieve this task, we must first import sqlalchemy.extract.
We created a new, empty list for june tempurature as j_temps. Next the query is pulling in the Measurements table, but only requested the tempuratures for the month of 6. Then turned j_temps into a list, then to a dataframe. From there we can see use describe() to see the summary statistics.

![june_sum_stat](https://user-images.githubusercontent.com/99375741/166160090-11d5b3e8-43d9-4bb1-9675-a7183d794f55.png)


### Deliverable 2: Determine Summary Stistic for December

For deliverable 2, we are determining the summary statistics for the tempurature in December. Like deliverable 1, we wrote a query to pull only data from the month of 12. Convered the data to a list, then converted it into a dataframe from which we can determine the summary statistic.

![dec_sum_stat](https://user-images.githubusercontent.com/99375741/166160114-9f580764-5e2c-4caa-a8e9-9e826e556fa1.png)


### Three main differences between June and December:
1. June temps have 1,700 records of daily tempuratures and Decemebr only has 1,517. There are 183 extra daily tempuratures for June. That is 6 months worth of December data that is missing. The data is no longer apples to apples.
2.  The standard deviation is greater in the December indicating the tempurature swings are worse during the winter, compared to the summer.
3.  Lastly, the lowest tempurature in December is 56 degrees, compared to the lowest in June, which is 64 degrees. That is a difference of 8 degrees. The highest temp in December is 83 degrees, compared to June, which is 85 degrees. That is a difference of 2 degrees. One can conclude the temprature margins are larger in December than in June.

## Summary

In the additional queries, we have found the summary statistics for June's and December's precipitation data. For both quesies, we filtered the Measurement table for only rows with the 6th and 12th months and precipitation data. We generated the summary statisics for June's and December's precipitation.

June Precipitation:

![june_precip](https://user-images.githubusercontent.com/99375741/166161271-0cfa05f3-17b5-4c27-8f74-f5f6177d6f0f.png)

December Precipitation:

![dec_precip](https://user-images.githubusercontent.com/99375741/166161283-dd5f6a97-14fc-489d-81a6-af8ceb925430.png)

The summary statistic for precipitation levels in June and December shows the precipitation is greater in December than in June. There is 59% more precipitation in December, than in June based on the means for each month.
