# Design of the Viseu Aerodrome Runway  
Final project developed in the Informatics, Systems and Programming discipline of the Master in Geographic Information Technologies of the University of Coimbra, taught by Dr. Alberto Jorge Lebre Cardoso in the academic year 2018-2019.

## Basic info

© Tiago Tamagusko (tamagusko@gmail.com) - [tamagusko.github.io](https://tamagusko.github.io)
<br> Version: 0.6 (2020/03/13)
<br> Using: Jupyter Notebook 6.0.2, Python 3.8, Linux 4.19.88-1-MANJARO x64, UTF-8.
<br> Required libraries: [requirements](/requirements.txt)
<br> Project Page: [github.com/tamagusko/ViseuAirportStudy](https://github.com/tamagusko/ViseuAirportStudy/)
<br> License: </a> 


## Problem

Viseu Aerodrome is interested in servicing bigger aircraft, which enable longer range and carry more passengers per aircraft [1](#1)</a>. This requires improving the structural strength of the pavement and increasing the length of its runway.

## Proposal

In order to design an airport pavement, it is necessary to know two main characteristics, namely the Pavement Classification Number¹ (PCN) and the extension of the runway.

Thus, the proposed challenge is to design a pavement with capacity (PCN) and extension to meet a desired group of routes.

## Project data structure:
    
    ├── 1-preprocessing.ipyng          # Database preprocessing 
    ├── 2-analysis.ipynb               # Data analysis
    ├── data                  
    │          ├── raw                 # Raw data
    │          ├── processed           # Data processed
    ├── reports                        # Outputs
    
## Notebooks:

1. Preprocessing - [1-preprocessing.ipyng](/1-preprocessing.ipynb)  
2. Analysis - [2-analysis.ipynb](/2-analysis.ipynb)

## Input data:

1. Aircraft database - [AircraftData.csv](/data/processed/AircraftData.csv)  
   a. **Aircraft**: Aircraft identification;  
   b. **ACN**²: Aircraft Classification Number;  
   c. **RequiredExtension**: Runway length required for landing and takeoff operations;  
   d. **Autonomy**: Aircraft autonomy;  
   e. **Passagers**³: Number of passengers carried.  
   **Updated: 25/12/2019**  

2. Airport database - [AirportData.csv](/data/processed/AirportData.csv)[2](#2)  
   a. **Airport ID**: 	Unique identifier for this airport;  
   b. **Airport**: Name of airport;  
   c. **City**:  Main city served by airport;  
   d. **Country**: 	Country or territory where airport is located;  
   e. **IATA**:  3-letter IATA code - **Unused data**;  
   f. **ICAO**:  4-letter ICAO code;  
   g. **Latitude**: 	Latitutide in decimal degrees. Negative is South, positive is North;  
   h. **Longitude** :	Longitude in decimal degrees. Negative is West, positive is East;  
   i. **Altitude**: 	Altitude in feet - **Unused data**;  
   j. **Timezone**: 	Hours offset from UTC  - **Unused data**;  
   k. **DST**: 	Daylight savings time. One of E (Europe), A (US/Canada), S (South America), O (Australia), Z (New Zealand), N (None) or U (Unknown)  - **Unused data**;  
   l. **Tz**: Timezone in "tz" (Olson) format, eg. "America/Los_Angeles" - **Unused data**;  
   m. **Type**: 	Type of the airport - **Unused data**;  
   n. **Source**: 	Source of this data - **Unused data**.  
   **Updated: 23/12/2019**  
3. Airport Database⁴ with extra data - [AirportExtraData.csv](/data/processed/AirportExtraData.csv)[3](#3)  
   a. **ICAO**:  4-letter ICAO code;  
   b. **RWYLenght**:  Runway length in meters;  
   c. **PCN**:  Runway structural strength number.  
   **Updated: 28/12/2019**  
4. Basemap shapefile - [20191227_basemap.shp](/data/processed/gis/20191227_basemap.shp)[4](#4)  
   a. Layer file with boundaries of countries;  
   **Updated: 28/12/2019**  
   
The data is UTF-8 encoded.

## Use:

**AnalysisByRWY(PCN, RWYLenght)**
> analysisByRWY(PCN, RWYLenght)  
Aircraft served: Aircrafts  
Routes served: Airports  

If you want to change the list of **aircraft** under study, edit the file: **Aircraft database (AircraftData.csv)**  
If you would like to change the list of **airports** under study, edit the file: **Airport extra database (AirportExtraData.csv)**

Notes: 

**¹** Indicates, among other elements, the structural strength of the pavement.  
**²** It is related to the impact of the aircraft on the pavement, and must be less than or equal to the runway PCN.  
**³** Information not required.  
**⁴** Shengen area airports only (lower airport security requirements).

# Results of Study:

![Results 20191229 by Tamagusko](https://github.com/tamagusko/ViseuAirportStudy/blob/master/reports/20191229Results.png)

[Download this file in format PDF](/reports/20191229Results.pdf)

# Future developments

1. Improve code with L.tooltip and json for leaflet:  
a. Change markers for airports;  
b. Put interactive labels (ICAO codes) for airports;  
c. Show legend with: Reference_Airport and Served_Airports

2. Rebuilding the functions for generic application, example:  
a. analysisByRWY(ReferenceAirport,PCN,RWYLenght);  

This study was not necessary as it is focused only on LPVZ (Viseu Airport).

3. Build/process a database with flight routes to evaluate possible connections.  
Interesting to see the range that the reference airport can have with a simple connection.

# Citation

Tamagusko, T. and Ferreira, A. (2020). Data Analysis applied to Airport Pavement Design, Submitted to Proceedings of the 6th International Conference on Road and Rail Infrastructure, Pula, Croatia.

Tamagusko, T. (2020). Airport Pavement Design. https://doi.org/10.13140/RG.2.2.19628.00640

```bibtex
@article{Tamagusko-Ferreira2020,
  author = {Tiago Tamagusko and Adelino Ferreira},
  title = {Data Analysis applied to Airport Pavement Design},
  journal = {Submitted to Proceedings of the 6th International Conference on Road and Rail Infrastructure},
  year = {2020},
  url = {https://github.com/tamagusko/ViseuAirportStudy}
}
@thesis{Tamagusko2020,
author = {Tamagusko, Tiago},
doi = {10.13140/RG.2.2.19628.00640},
number = {February},
pages = {82},
school = {University of Coimbra},
title = {{Airport Pavement Design}},
type = {Master Dissertation in Urban Mobility Management},
year = {2020}
url = {https://doi.org/10.13140/RG.2.2.19628.00640}
}
```

# References

<a id="1">[1]</a> 
Martins, J. P. F. (2018). 
Reflexão sobre a viabilidade e localização de uma infraestrutura aeroportuária na região Centro de Portugal (Universidade do Porto). 
https://doi.org/10.13140/RG.2.2.34944.69124 

<a id="2">[2]</a> 
OpenFlights (2019). 
Airport, airline and route data. 
Retrieved December 23, 2019, from https://openflights.org/data.html 

<a id="3">[3]</a> 
World Aero Data (2019). 
World Aeronautical Database. 
Retrieved December 28, 2019, from https://worldaerodata.com 

<a id="4">[4]</a> 
Natural Earth (2019). 
Free vector and raster map data at 1:10m, 1:50m, and 1:110m scales. 
Retrieved December 25, 2019, from http://www.naturalearthdata.com 
