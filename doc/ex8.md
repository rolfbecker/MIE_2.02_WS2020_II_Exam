# Exercise 8: Dimension a roof drainage for two new industrial buildings.

A new industrial facility with two buildings is planned in the county of Olpe. 
The water raining on the roof of the buildings has to be drained. 
To plan the drainage system you have to determine the total amount of water collected by the roofs in the 
four months May to August 2017. Assume that the annual precipitation sum is approximately 3 x the 
precipitation sum over the four months. 

Unfortunately you just have a bad photography (a screenshot taken with a camera :-) ) of the roof plan. You have to georeference and 
digitize this photo first to determine the roof area and location. 
Then you have to multiply the cumulative annual precipitation for the location of the roofs with the total roof 
area to get the collected total annual precipitation volume in m³/year. 
To get the precipitation falling on the roofs you can assume that the precipitation 
does not vary across the roofs. 

However, you do not have a precipitation station at the location of the planned buildings. 
How to deal with that?
There are serveral methods to estimate the local precipitation from measurements at the distributed 
DWD stations. The simplest way would be the method of nearest neighbor. 
A more sophisticated method is that of a linear estimator with weights proportional 
to inverse distances between the location of interest and the precipitation stations around. 
Find out how the inverse distance interpolation works and determine the annual cumulative precipitation at the location of the 
new buildings as well as the total rain water volume collected by their roofs during 2017. 

How much water do you have to drain? 


## Load Digital Ortophotos Web Mapping Services (WMS)
From this link: *https://www.bezreg-koeln.nrw.de/brk_internet/geobasis/luftbildinformationen/aktuell/digitale_orthophotos/index.html*
you can get the product of Digital Ortophotos(DOP) of NRW as WMS with 10cm ground sampling distance (GSD).

Find out how to load this WMS layer in QGIS.

## Georeference and digitize the roof area
The folder *./data/original/Industrial_area/* a scan of the draft of the roof plan. Open the scan draft
and try to locate this area in the digital ortophotos (DOP). **Hint:** the approximate coordinates of the 
traffic roundabout of the scan are *[423987,5665648] EPSG: 25832.*

Then, go to raster-> Georeferencer and load the scan. Now you can start georeferencing the roof plan of the buildings.

Remember that you need several control points for the geoferencing algorithm to work correctly.
 
## Calculate the area of the roof
After correctly digitizing the roof of the two buildings, it should be relatively straight forward to 
calculate the area of it. You could for example create two polygons overlaying with the 
resulting georeferenced layer.

## Interpolate cumulative precipitation
QGIS has different tools for interpolation. We suggest both nearest neighbors and inverse weight distances. Compare the results of these two inperpolation methods for your case.
Find out how to make it work with your data. You should estimate the total rain water volume collected by both roofs 
during 2017. Assume that the annual precipitation sum is approximately 3 x the 
precipitation sum over the four months.  

## Discuss your findings
You should integrate the whole activity in the final report. Are your results plausible? How accurate can
they be?


* [Previous](ex7.md)

