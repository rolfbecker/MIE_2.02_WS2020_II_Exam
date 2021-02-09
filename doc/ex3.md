# Exercise 3: Generate precipitation video in QGIS
Developing Exercise precipitation video...

Among other factors the soil moisture index (SMI) is influenced by precipitation. If you have ongoing evaporation from the soil and transpiration by the plants soil water is transported into the atmosphere. Without precipitation the soil moisture would deplete and the SMI would decline.

To get an overview of the spatio-temporal precipitation development in the federal state of Nordrhein-Westfalen (NRW) create a video using the time manager plugin of QGIS. Show the precipitation dynamics for **all DWD stations in NRW with hourly precicipitation measurements for the half open interval [2017-06-16T00:00:00Z, 2017-06-17T00:00:00Z)**. 

The two SMI maps for month June and July are snapshots at 2017-06-16 and 2017-07-16, respectively. The step from June to July shows the strongest change of SMI during the total period analysed.

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

* [Previous](ex2.md)
* [Next](ex4.md)
