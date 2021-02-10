# Exercise 1: Generate a Map

This exwercise helps you to locate the study area and to identify the
information available in the region.
You are interested in the distribution of weather stations that offer hourly precipitation
data in the 13 counties selected for the study. Moreover, you want to include the topography (altitude)
of the counties of interest, in order to look at possible correlations between precipitation and terrain altitude.
You should generate a map of the 13 counties of interest, the active precipitation stations (hourly values, active in 2017) within them, and 
the Digital Terrain Model (DTM) of the region.

## Load the vector layers corresponding to the counties of interest
The folder */data/original/Counties_Municipalities_NRW/* provides a geopackage with the 
13 counties of interest, as well as the municipalities of whole NRW.

Open the vector layers in QGIS. And perform the geoprocessing steps required.

## Download and process DWD weather stations description file

You should generate a point vector layer for QGIS containing the location of all active weather stations in the year 2017 which provide hourly precipitation data. This is already "historical" data. We performed similar tasks in the lecture. Find an appropriate notebook to start with. Change it to historical data. You can use the CSV import method for QGIS we discussed in the lecture or use Geopandas to create the vector layer directly. 

## Download DTM data for the area of interest
Given the spatial extent of the area of interest, you can use a lower resolution DTM for this
part of the analysis. You can find the DTM for the region of NRW with 50m resolution following
this link: https://data.opendataportal.at/dataset/dtm-germany/resource/c6aae7d1-c9dc-4e44-a9b2-10be2ed25dfe

Find an appropiate color representation after loading it in QGIS. Find out how to improve the
DTM representation e.g. give it some texture by generating a Hill Shade Model and overlaying it
with the colored DTM using transparency options.

## Generate a Map
After the previous preparation you should generate a proper map using the layers generated.
You should consider the following:
- The 13 counties of interest should be clearly visible and easy to differentiate.
- Display the names of the counties in an organized manner. 
- Correct color representation of the DTM.
- The location of the active precipitation weather stations should be easy to recognize (appropriate symbology and labels).
- Use the stations ID for the labels.
- The map should include scale and nord arrow.
- Take care of the label style, the map should not be cluttered, use correct symbology...   

* [Next](ex2.md)
