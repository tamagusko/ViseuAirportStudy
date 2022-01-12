## Input data:

1. Aircraft database - [AircraftData.csv](/data/processed/AircraftData.csv) [[1]](#1)  
   a. **Aircraft**: Aircraft identification;  
   b. **ACN**²: Aircraft Classification Number;  
   c. **RequiredExtension**: Runway length required for landing and takeoff operations;  
   d. **Autonomy**: Aircraft autonomy;  
   e. **Passagers**³: Number of passengers carried.  
   **Updated: 25/12/2019**

2. Airport database - [AirportData.csv](/data/processed/AirportData.csv) [[2]](#2)  
   a. **Airport ID**: Unique identifier for this airport;  
   b. **Airport**: Name of airport;  
   c. **City**: Main city served by airport;  
   d. **Country**: Country or territory where airport is located;  
   e. **IATA**: 3-letter IATA code - **Unused data**;  
   f. **ICAO**: 4-letter ICAO code;  
   g. **Latitude**: Latitutide in decimal degrees. Negative is South, positive is North;  
   h. **Longitude** : Longitude in decimal degrees. Negative is West, positive is East;  
   i. **Altitude**: Altitude in feet - **Unused data**;  
   j. **Timezone**: Hours offset from UTC - **Unused data**;  
   k. **DST**: Daylight savings time. One of E (Europe), A (US/Canada), S (South America), O (Australia), Z (New Zealand), N (None) or U (Unknown) - **Unused data**;  
   l. **Tz**: Timezone in "tz" (Olson) format, eg. "America/Los_Angeles" - **Unused data**;  
   m. **Type**: Type of the airport - **Unused data**;  
   n. **Source**: Source of this data - **Unused data**.  
   **Updated: 23/12/2019**

3. Airport Database⁴ with extra data - [AirportExtraData.csv](/data/processed/AirportExtraData.csv) [[2]](#2)  
   a. **ICAO**: 4-letter ICAO code;  
   b. **RWYLenght**: Runway length in meters;  
   c. **PCN**: Runway structural strength number.  
   **Updated: 28/12/2019**

4. Basemap shapefile - [20191227_basemap.shp](/data/processed/gis/20191227_basemap.shp) [[3]](#3)  
   a. Layer file with boundaries of countries;  
   **Updated: 28/12/2019**

The data is UTF-8 encoded.

## References

[1] 
World Aero Data (2019). 
World Aeronautical Database. 
Retrieved December 28, 2019, from https://worldaerodata.com

[2] 
OpenFlights (2019). 
Airport, airline and route data. 
Retrieved December 23, 2019, from [OpenFlights: Airport and airline data](https://openflights.org/data.html)

[3] 
Natural Earth (2019). 
Free vector and raster map data at 1:10m, 1:50m, and 1:110m scales. 
Retrieved December 25, 2019, from [Natural Earth - Free vector and raster map data at 1:10m, 1:50m, and 1:110m scales](http://www.naturalearthdata.com)
