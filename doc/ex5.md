# Exercise 5: Calculate cumulative precipitation time series
Developing cumulative precipitation time series...

In this section you want to narrow down your area of study. You have noticed the strong differences of 
SMI between Olpe and Hochsauerlandkreis for the months of May and June of 2017. These response is 
atenuated in July, and in August the SMI is almost homogenous. How can you explain this?
Does it have something to do with precipitation events? You will have to use the precipitation
data offered by the German Weather Service (DWD) to find out.

### Aggregate hourly precipitation to achieve daily resolution
Use the notebook provided in order to filter and aggregate your precipitation measurements.
You should narrow down this analysis for the weather stations of
counties of Olpe and Hochsauerlandkreis. 
From your hourly values. Write a script to aggregate the data to an hourly resolution. 

### Cumulative precipitation time series
You should generate two diagrams: 

- A bar chart of the daily precipitation covering the four months of the study 
(from 2017.04.16 until 2017.08.16)to identify interesting precipitationevents
- A scatter plot of the cumulative precipitation (amount of water in time) for the same time period.

You should consider the following:
- Think about how to organize the representation. 
You are generating graphs from approx. 15 weather stations (maybe using facets?)
- Correct labeling of your graphs. Use legends when appropiate 
- The images should be tidy. Take care of oclusions of graphs that are not readable.
- Make sure to include relevant information in your plots, such as resolution, units, time period...

