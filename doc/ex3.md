# Exercise 2:Generate SMI maps of the counties of interest for the selected dates  


Developing Exercise SMI maps...

In this section you will produce four maps that reflect the SMI for the counties of interest for
the **16th of May, June, July and August in 2017**. 

### Load the vector layers corresponding to the counties of interest
[See Exercise 2](ex2.md)

### Load the SMI layers for Germany
You will use soil moisture index data for germany in the topsoil layer. 
This data is provided by  UFZ Drought Monitor / Helmholtz Centre for Environmental Research. 
The original dataset can be downloaded in Netcdf format from https://www.ufz.de/index.php?en=37937 
and covers the period between 1951 and 2018. In order to save you some time we have extracted 
the dates that are interesting for this report. You can find the layers in the folder 
*/data/original/SMI/*.

Make sure that you are using an appropiate color representation. In */data/original/SMI/* we provided
you with a color map file: *"SMI_color_scale_XXX.txt"*. 
You can use it in your SMI layers so that all have the same representation.

Perform the appropiate processing so you end up with a layer suitable for mapping. Remember that you
should focus in the 13 counties of interest.

#### Generate four maps
After the previous preparation you should generate four proper SMI maps.
You should consider the following:
- The 13 counties of interest should be clearly visible and easy to differentiate.
- Display the names of the counties in an organized manner. 
- Correct color representation of the SMI.
- **TENTATIVE** The location of the active precipitation weather stations should be easy to recognize.
- **TENTATIVE** Use the stations ID for the labels.
- **TENTATIVE** Make sure that you can differentiate between stations displaying precipitation-only,
temperature-only, and both observations.
- The maps should include scale and nord arrow.
- Take care of the label style, the map should not be cluttered, use correct symbology...
- Make sure to include important metadata in your maps such as sensing date, resolution and sources.
- You can display these maps in an 2x2 array manner.  

* [Previous: Exercise 2](ex2.md)
* [Next: Exercise 4](ex4.md)
