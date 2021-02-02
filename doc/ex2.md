# Exercise 2: Generate a Map
Developing Exercise Map precipitation stations...

This section of the project will serve to locate the study area and to identify the
information available in the region
You are interested in the distribution of weather stations that offer hourly precipitation
data in the counties selected for the study. Moreover, you want to include the altitude profile
of the counties of interest, in order to look at possible correlations of altitude and precipitation.
You should generate a Map of the counties of interest, the active weather stations within them, and 
the Digital Terrain Model of the region.
### Load the vector layers corresponding to the counties of interest
The folder */data/original/Counties_Municipalities_NRW/* provides a geopackage with the 
counties of interest, as well as the municipalities of whole NRW.

Open the vector layers in QGIS. And perform the geoprocesing steps required.

### Download and process DWD weather stations description file
The folder */jupyter/* contains a jupyter notebook similar to the one used in the lecture.

You should generate a point vector layer for QGIS containing the location of all weather
stations active weather stations in the year 2017 which provide hourly precipitation data.

**TENTATIVE** Additionally, generate another point vectot layer with the location of all active 
weather stations providing hourly temperature data for the same year. Generate a third point
layer with the stations providing both observations.

### Download DTM data for the area of interest
Given the spatial extend of the area of interest, you can use a lower resolution DTM for this
part of the analysis. You can find the DTM for the region of NRW with 50m resolution following
this link: https://data.opendataportal.at/dataset/dtm-germany/resource/c6aae7d1-c9dc-4e44-a9b2-10be2ed25dfe

Find an appropiate color representation after loading it in QGIS. Find out how to improve the
DTM representation e.g. give it some texture by generating a Hill Shade Model and overlaying it
with the colored DTM using transparency options.

### Generate a Map
After the previous preparation you should generate a proper map using the layers generated.
You should consider the following:
- The 13 counties of interest should be clearly visible and easy to differentiate.
- Display the names of the counties in an organized manner. 
- Correct color representation of the DTM.
- The location of the active precipitation weather stations should be easy to recognize.
- Use the stations ID for the labels.
- **TENTATIVE** Make sure that you can differentiate between stations displaying precipitation-only,
temperature-only, and both observations.
- The map should include scale and nord arrow.
- Take care of the label style, the map should not be cluttered, use correct symbology...   

[Previous: Exercise 1](ex1.md)
[Next: Exercise 3](ex3.md)