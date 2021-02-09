# Exercise 4: Generate precipitation video in QGIS
Developing Exercise precipitation video...

You should develop a video using the time manager function of QGIS. You are interested in showing
the precipitation dynamics in the counties of interest. You should use hourly precipitation data
from the German Weather Service (DWD) for a total of one month (The strongest change of SMI during the 
period analysed).

### Download and process climate data
In the folder */./jupyter/* you will find a jupyter notebook script similar to the one we developed
in the lecture. Modify in order to retrieve hourly precipitation measurements that correspond 
to the sensing dates of the SMI strongest change of the time span analysed 
(16th June until 16th July 2017). 

You want to shape your data in such a way that it is readable in QGIS.

Take care of the representation of the measurements. You should use appropiate color scales.

### **TENTATIVE** Load the data in a PSQL database
**Give indications on retrieval and linking of data with time manager**

### Generate one month video of daily precipitation
After the previous preparation you should generate a video of daily precipitation corresponding to one
month of data.

You should consider the following:
- Appropiate color representation
- You should identify interesting precipitation events that you can link to the changes of SMI.
- You should provide a link to this video in your final report. 

* [Previous: Exercise 3](ex3.md)
* [Next: Exercise 5](ex5.md)