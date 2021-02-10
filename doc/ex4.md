# Exercise 4: Calculate cumulative precipitation time series

In this section you want to narrow down your area of study. You have noticed the strong differences of 
SMI between Olpe (OE) and Hochsauerlandkreis (HSK) for the months May and June 2017. The difference 
decreases in July, and in August the SMI become quite similar. How can you explain this?
Does it have something to do with precipitation events? You will have to use the precipitation
data offered by the German Weather Service (DWD) to find out.

## Aggregate hourly precipitation rate to achieve daily precipitation rate

To identify rain events you will plot daily precipitation in a vertical bar chart. You have to aggregate the hourly precipitation rate (mm/hr) over a day to yield the daily precipitation rate (mm/day). 
Use the notebook provided in order to filter and aggregate your precipitation measurements.
You should narrow down this analysis for the weather stations of
counties of Olpe and Hochsauerlandkreis. Write a Python/Pandas script to aggregate the data to daily resolution. Consider to use the Pandas Dataframe function `df.group_by(...)`.

### Cumulative precipitation time series
You should generate two diagrams: 

- A bar chart of the daily precipitation rates (mm/day) covering the four months of the study 
(from 2017-04-16 until 2017-08-16) to identify interesting precipitation events
- A line graph showing the cumulative precipitation for the same period.

You should consider the following:
- Think about how to organize the representation. 
You are generating several graphs in one diagram from weather stations in OE and HSK (maybe using facets?)
- Correct labeling of your graphs. Use legends when appropiate 
- The images should be tidy. Take care of oclusions of graphs that are not readable.
- Make sure to include relevant information in your plots, such as time resolution, 
units, time period...

* [Previous](ex3.md)
* [Next](ex5.md)
