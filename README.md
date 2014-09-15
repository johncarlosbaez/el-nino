## Experiments in El Nino analysis and prediction

This software is connected to the Azimuth Code Project **[Experiments in El Nino analysis and prediction](http://www.azimuthproject.org/azimuth/show/Experiments%20in%20El%20Ni%C3%B1o%20analysis%20and%20prediction)**.  

#### R / netcdf-convertor-ludescher.R

This script written by Graham Jones converts netCDF files containing daily mean surface temperature data from NOAA (e.g. air.sig995.1951.nc) into a format more easily readable by other programs in other languages.  You need to have installed the package [RNetCDF](http://cran.r-project.org/web/packages/RNetCDF/index.html) to use this scipt.   You can edit it in these ways to meet your requirements:

* change the ranges of latitude and longitude
* change the range of years

As supplied, it converts the data from 1948 to 1949 in a region of the Pacific used in a [paper by Ludescher *et al*](http://www.pnas.org/content/early/2013/06/26/1309353110.full.pdf+html).  Then start R, and copy and paste the 
whole file into the R console. (There are other ways of running R scripts but this is simplest for novices.)

More instructions are in the script itself.  For even more detailed explanations, see [Part 4](http://johncarlosbaez.wordpress.com/2014/07/08/el-nino-project-part-4/) and [Part 5](http://johncarlosbaez.wordpress.com/2014/07/12/el-nino-project-part-5/) of the El Ni&ntilde;o Project series on the Azimuth blog.

#### R / ncdf-convertor.R

This is a modified version of the above script made by Benjamin Antieau, who was unable to get RNetCDF to work on OS 10.9 Mavericks.  This uses the R package [ncdf](http://cran.r-project.org/web/packages/ncdf/index.html) instead.  For a comparison of these packages, read [this](http://r.789695.n4.nabble.com/big-difference-between-ncdf-and-RNetCDF-td4676332.html).

#### R / nino3.4-anoms.txt

This is a copy of the [monthly Niño 3.4 index](http://www.cpc.noaa.gov/products/analysis_monitoring/ensostuff/detrend.nino34.ascii.txt) from the [US National Weather Service](http://www.cpc.noaa.gov/products/analysis_monitoring/ensostuff/detrend.nino34.ascii.txt); the copy was made in July 2014 and contains data from 1948 to 2013.  It has monthly Niño 3.4 data in the column called ANOM.

#### R / ludescher.R

This program is aimed at replicating the  [paper by Ludescher *et al*](http://www.pnas.org/content/early/2013/06/26/1309353110.full.pdf+html).  To run it, you need to have the files
`Pacific-1948-1980.txt` (created using the above program, netcdf-convertor-ludescher.R) and `nino3.4-anoms.txt` in your working directory for R.

For detailed explanations of what the program does, see [Part 3](http://johncarlosbaez.wordpress.com/2014/07/01/el-nino-project-part-3/) and [Part 4](http://johncarlosbaez.wordpress.com/2014/07/08/el-nino-project-part-4/) of the El Ni&ntilde;o Project series.

#### R / average-link-strength.R

This file has the average link strength S as computed by `ludescher.R` at 10-day intervals, starting from day 730 and going until day 12040, where day 1 is the first of January 1948.  For an explanation see  [Part 4](http://johncarlosbaez.wordpress.com/2014/07/08/el-nino-project-part-4/) of the El Ni&ntilde;o Project series.

#### R / grj / covariances-basin-vs-rest.R

Makes maps of the Pacific, one per quarter from 1951 to 1979, showing covariances of grid points with the 'Ludescher et al basin'.

```
