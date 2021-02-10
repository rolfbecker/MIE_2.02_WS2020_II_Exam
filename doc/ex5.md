# Exercise 5: Analyse cumulative precipitation vs altitude (DTM)

Investigate the relationship of cumulative precipitation and altitude of the precipitation stations for all stations located in the 13 counties. Take the station altitudes from the station description file (station metadata). Sum up the precipitation per station for the four months May, June, July and August 2017 (one total rainfall value per station) and plot it vs. altitude. Do you see a relationship? 

Create a map with the precipitation stations of the 13 counties together with the DTM 50m (similar to previous exercises). Change the stations' symbol color according to the precipitation sum (total rainfall) over the four months. Do you see a relationship between total rain water gathered in four months and the station altitude?

Compare the station altitudes given in the station metadata with the DTM altitudes at the station locations. You can sample the DTM at the point features of the station layer easily and add this information to the attribute table of the station layer. Plot the differences between the two altitude values for the stations. Waht do you observe? Where do these diferences come from? What do you think: Which one would be more precise? Explain.

You should consider the following:
- You can directly compare the altitude values by using a nx2 table. Where n is the number of 
weather stations compared.
- Make sure to somehow indicate strong differences. You should try to find an explanation for them and
indicate which measure should be more reliable.
- Figure out if you can plot final value of cumulative precipitation VS Altitude of weather station.
- Is the result what you expected? Is there a tendency? are there outliers? Make sure to include
all that in your discussion.

* [Previous](ex4.md)
* [Next](ex6.md)
