# PyBer_Analysis

## Project Overview

Senior management at PyBer has requested an analysis of ride-sharing data from multiple cities in order to gain insight into the data. In order to complete the analysis two deliverables that provide answers to a number of queries must be created:

    1. A summary DataFrame that includes:
        - The total number of rides for each city type.
        - The total number of drivers for each city type.
        - The total fares for each city type.
        - The average fare per ride for each city type.
        - The average fare per driver for each city type.
    2. A line graph showing total fares by city type on a weekly basis. 

### Resources

- Data Source: city_data.csv, ride_data.csv
- Software: Python 3.7.1, Visual Studio Code 1.71, Anaconda 4.14.0, Jupyter Notebook 6.4.8, Pandas 1.4.3, Matplotlib 3.5.1

## Results

### Summary DataFrame.

To begin the analysis, the two csv files that hold the PyBer data are loaded into DataFrames, these two DataFrames are subsequently merged to create a new DataFrame that contains all of the available data. From this merged DataFrame the information for the summary DataFrame is collected into multiple Series. Once all the necessary Series are created, each of them is added to the final summary DataFrame. Once the new DataFrame is formatted the first deliverable is complete.

![pyber_summary_df.png](https://github.com/Jforbus/PyBer_Analysis/blob/main/Resources/pyber_summary_df.png)

This DataFrame contains some very valuable information. First, it shows that Urban cities account for 13 times as many rides as Rural cities. There are 5 times as many Suburban rides as Rural Rides. The majority of Total Rides are in Urban cities. An even more extreme disparity exists in the Total Drivers column, with Urban drivers making up over 30 times more of the driver population than Rural Drivers, and nearly 5 times more than Suburban drivers. Fare Totals follow the previous trend in the data, with Rural cities only earning 6.8% of the Fare Totals. Urban cities earned 62.7% of the Fare Totals, and Suburban cities received 30.5% of the Total Fares. Along with these discoveries, the DataFrame shows that the average fare per ride and per driver are much higher in Rural cities. Riders in Rural cities pay on average 30% more per ride than riders in Urban cities. This is mirrored by a significant increase in the average fare per driver in Rural cities versus Urban cities. Drivers in Rural cities earn a significantly larger amount per ride than those in Urban cities. Throughout this table, the numbers for Suburban city types have consistently presented between the Urban and Rural numbers. The data shows that where Ride and Driver Totals are higher, and Average Fares lower, the Total Fares are much higher. 

### Weekly Fare by City Type Line Graph.

Secondly, the line graph must be created. To do this a pivot table is created from the merged DataFrame that indexes the ride data by date, and provides the city type and fare for each ride.
From this pivot table the section of time to be graphed is selected, organized into weekly bins that hold the total fares for the week for each city type, and converted into a new DataFrame. The graph is then created from this DataFrame.

![PyBer_fare_summary.png](https://github.com/Jforbus/PyBer_Analysis/blob/main/Analysis/PyBer_fare_summary.png)

The graph gives another revelatory perpective on the data. It shows that each of the city types brings in a very different share of the total fares in each week. Each city type occupies its own tier on the graph: Urban from 1500 to 2500, Suburban from 500 to 1500, and Rural from 0 to 500. There is a peak in the total fares for all 3 city types a week prior to the end of February. These simultaneous peaks suggest a corresponding event to the rise in total fares that transcends the city type. Overall the graph shows that the total weekly fares remain relatively consistent across the timeframe measured, and Suburban Fare Totals stayed between Urban and Rural Fare Totals for the duration of the graphed data. 


## Summary

The analysis shows that where ride totals are higher, fares are lower and fare totals are higher. Fare per driver and per ride is also lower than where fare totals are lower. There is likely a correlary attribute associated with the city type that leads to the drastically higher ride totals in Urban cities versus Rural cites. Population density differences, demographic differences, marketing limits, and many other factors could be contributing to the disparity in the data. In order to address the differences in the data, Pyber will need to increase Ride Totals for Rural cities drastically, along with raising Ride Totals in Suburban cities. Suggestions for PyBer to approach this are:

1. Increase Marketing efforts to Rural and Suburban cities to gain more interest in the service, increasing ride totals. 
2. Recruit more Drivers in Rural and Suburban cities. Urban cities have a significantly higher Driver Totals. Increased Driver availability could lead to higher Ride Totals and Fare Totals in Rural and Suburban cities.
3. Decrease Average Fares in Rural and Suburban cities. Fares are higher on average in these city types. Higher fares could be deterring customers, driving down Ride Totals in Rural and Suburban cities. 
