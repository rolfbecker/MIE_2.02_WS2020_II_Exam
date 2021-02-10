# Exercise 3: Generate a precipitation video in QGIS

Among other factors the soil moisture index (SMI) is influenced by precipitation. If you have ongoing evaporation from the soil and transpiration by the plants soil water is transported into the atmosphere. Without precipitation the soil moisture would deplete and the SMI would decline.

To get an overview of the spatio-temporal precipitation development in the federal state of Nordrhein-Westfalen (NRW) create a video using the time manager plugin of QGIS. Show the precipitation dynamics for **all DWD stations in NRW with hourly precipitation measurements for the half open interval [2017-06-16T00:00:00Z, 2017-06-17T00:00:00Z)**. 

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

## Method 1: Use Python/Pandas

We used this method in class. Download via FTP the station description file as well as the relevant time series. Perform a join (merge) and save the relation as CSV. Import it into QGIS and apply the TM. **You will find the notebooks to start with in the Git repository of the course**. You will have to adapt the notebooks to read hourly historical (2017) precipitation data.  

Take care of the representation of the measurements in QGIS. Use appropiate mapping and color scales.

## Method 2: Use PostGIS (much cooler, yields extra points!)

This method has a much better performance. In principle it can handle big data (e.g. long time series for all stations in Germany) flexibly. The idea is to insert the station information as a vector layer with relation schema (station_id, name, altitude, geometry(point)) into a PostGIS enabled ProstgreSQL database and to insert precipitation time series data in a relation of schema (station_id (numeric(6,0)), ts (timestamp with time zone), val (REAL)). Then you create a view joining station info (providing a geometry column with station location points) and time series on station_id yielding the above mentioned 1:N relationship. This view can be used in QGIS. Import it via the menu 
`Layer -> Add Layer -> Add PostGIS Layers ...`   

You will find additional information in the new repository https://github.com/rolfbecker/opengeo . We use it to reorganize part of our training material. It is under construction and incomplete. Anyway, have a look at activity geo0930.

* [Previous](ex2.md)
* [Next](ex4.md)
