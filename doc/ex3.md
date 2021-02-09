# Exercise 3: Generate a precipitation video in QGIS
Developing Exercise precipitation video...

Among other factors the soil moisture index (SMI) is influenced by precipitation. If you have ongoing evaporation from the soil and transpiration by the plants soil water is transported into the atmosphere. Without precipitation the soil moisture would deplete and the SMI would decline.

To get an overview of the spatio-temporal precipitation development in the federal state of Nordrhein-Westfalen (NRW) create a video using the time manager plugin of QGIS. Show the precipitation dynamics for **all DWD stations in NRW with hourly precicipitation measurements for the half open interval [2017-06-16T00:00:00Z, 2017-06-17T00:00:00Z)**. 

The two SMI maps for month June and July are snapshots at 2017-06-16 and 2017-07-16, respectively. The step from June to July shows the strongest change of SMI during the total period analysed.

## QGIS TimeManager plugin

The TimeManager (TM) plugin allows you to display snapshots of time-varying attribute data of vector layers. Before you can use the TM some data processing is necessary to provide the right data format to the TM. Technically you have to realize a 1:N relationship between two relations: (1) station info (including geodata/coordinates) with key (station_id) and (2) the time varying precipitation measurements with key (station_id, timestamp).  

Each precipitation station has to be joined with its prec time series consisting of N measurements externally, e.g. done with Pandas/Python and stored as CSV. Each station is copied N times. Each copy is then extended with the actual measurement for a given time. In QGIS these features sharing the same location (i.e. station information) are plotted on top of each other. The data is highly redundent. This is done for all stations in a region of interest and all measurement times in the time series data.

The Time Manager just selects features (i.e. stations with individual prec values) for a given time stamp. That means for a given selection time only N stations with their prec values are remaining and displayed. In this way you can create a sequence of maps showing the precipitation distribution across the stations for each measurement time. These maps can be stored as images which can be combined to a video in post processing.


| station_id |        name        |   lat   |   lon  |        meas_time       | prec_rate |
|:----------:|:------------------:|:-------:|:------:|:----------------------:|:---------:|
|        ... | ...                |     ... |    ... |                    ... |       ... |
|       1595 | Gelsenkirchen-Buer | 51.5762 | 7.0652 | 2017-06-07T08:00:00UTC |       1.5 |
|       1595 | Gelsenkirchen-Buer | 51.5762 | 7.0652 | 2017-06-07T09:00:00UTC |       1.7 |
|       1595 | Gelsenkirchen-Buer | 51.5762 | 7.0652 | 2017-06-07T10:00:00UTC |       0.1 |
|        ... | ...                |     ... |    ... |                    ... |       ... |
|      13670 | Duisburg-Baerl     | 51.5088 | 6.7018 | 2017-06-07T08:00:00UTC |       0.8 |
|      13670 | Duisburg-Baerl     | 51.5088 | 6.7018 | 2017-06-07T09:00:00UTC |       0.4 |
|      13670 | Duisburg-Baerl     | 51.5088 | 6.7018 | 2017-06-07T10:00:00UTC |       0.0 |
|        ... | ...                |     ... |    ... |                    ... |       ... |

*Table: Example of a relation suited for the TimeManager. The primary key of this example relation is (station_id, meas_time).*

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
