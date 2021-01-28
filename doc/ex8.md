# Exercise 8: NDVI
Developing NDVI exercise...

You want to assess if the strong changes observed in the SMI between April-/May-2017, and May-/June-2017 
can also be appreciated by analysing the NDVI of a subset of areas of interest in the
the municipality of Olpe.

Three different towns were preselected for this analysis. 
You will be assigned two different areas of interest for each town. One for each field type: 
*"Ackerland"* (in english arable land / fields) and *"Grünland"* (in english grassland) 

### Identify the fields of interest assigned to your group

The folder */data/original/agricultural_areas_of_interest* provides a geopackage file with all 
numbered ROIs as well as the file *ROI_assignment.csv* containing the list of select polygon numbers
for each student working group.

Open the geopackage with all predefined ROIs in QGIS.

Select only the polygons assigned to your team. 
Use the above mentioned CSV file with the polygon IDs for your group.

### Download Sentinel-2 multispectral imagery
You have to analyze the period April-June of 2017 of the municipality of Olpe.
Put emphasis on your subset of ROIs. The land-use areas (polygons) of concern may encompass
more than one NDVI pixel. Think about how to deal with it.

In order to save you some time we have identified three appropiate sensing
dates with low cloud coverage:
**(a) 2017-05-10, (b) 2017-06-19, (c) 2017-07-19.**
Download and store the images in an appropiate folder. Make sure that the Sentinel 
product you use is processed up to level-2A Bottom of Atmosphere (BOA) reflectance. 

### Analyse the data and compare
 Are there interesting changes in NDVI in your ROIs? 
 are these changes depending on the field type? Does it correspond to the
behaviour of the SMI for the same regions? How can you explain these results?
Additionally, you can use the true color images (TCI)in the Sentinel-2 products in order 
to better inspect the ROIs within the visual spectrum.

Perform the core analysis with respect to your research questions.
Write an appropriate report according to the guidelines of scientific writing. 
Always think about the intention of your investigation and the reader! 
The text has to be well structured and formulated.








