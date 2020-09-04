<h1>Design of the Viseu Aerodrome Runway</h1>
Final project developed in the Informatics, Systems and Programming discipline of the Master in Geographic Information Technologies of the University of Coimbra, taught by Dr. Alberto Jorge Lebre Cardoso in the academic year 2018-2019.

<h2>Basic info</h2>

© Tiago Tamagusko (tamagusko@gmail.com) - <a href="https://tamagusko.github.io">https://tamagusko.github.io</a>
<br> Version: 0.6 (2020/03/13)
<br> Using: Jupyter Notebook 6.0.2, Python 3.8, Linux 4.19.88-1-MANJARO x64, UTF-8.
<br> Required libraries: <a href="/requirements.txt">requirements</a>
<br> Project Page: <a href="https://github.com/tamagusko/ViseuAirportStudy/">github.com/tamagusko/ViseuAirportStudy</a>
<br> License: <a href="/LICENSE.md">Apache-2.0</a>


<h2>Problem</h2>

Viseu Aerodrome is interested in servicing bigger aircraft, which enable longer range and carry more passengers per aircraft <a href="https://github.com/tamagusko/ViseuAirportStudy/blob/master/README.md#-references">[1]</a>. This requires improving the structural strength of the pavement and increasing the length of its runway.

<h2>Proposal</h2>

In order to design an airport pavement, it is necessary to know two main characteristics, namely the Pavement Classification Number¹ (PCN) and the extension of the runway.

Thus, the proposed challenge is to design a pavement with capacity (PCN) and extension to meet a desired group of routes.

<h2>Project data structure:</h2>
    
    ├── 1-preprocessing.ipyng          # Database preprocessing 
    ├── 2-analysis.ipynb               # Data analysis
    ├── data                  
    │          ├── raw                 # Raw data
    │          ├── processed           # Data processed
    ├── reports                        # Outputs
    
<h2>Notebooks:</h2>

1. Preprocessing  - <a href="/1-preprocessing.ipynb">1-preprocessing.ipyng</a> 

2. Analysis  - <a href="/2-analysis.ipynb">2-analysis.ipynb</a> 

<h2>Input data:</h2>

1. Aircraft database - <a href="/data/processed/AircraftData.csv">AircraftData.csv</a>
   <br>a. **Aircraft**: Aircraft identification;
   <br>b. **ACN**²: Aircraft Classification Number;
   <br>c. **RequiredExtension**: Runway length required for landing and takeoff operations;
   <br>d. **Autonomy**: Aircraft autonomy;
   <br>e. **Passagers**³: Number of passengers carried.
   <br> **Updated: 25/12/2019**

2. Airport database  - <a href="/data/processed/AirportData.csv">AirportData.csv</a> <a href="https://github.com/tamagusko/ViseuAirportStudy/blob/master/README.md#-references">[2]</a> 
   <br>a. **Airport ID**: 	Unique identifier for this airport;
   <br>b. **Airport**: Name of airport;
   <br>c. **City**:  Main city served by airport;
   <br>d. **Country**: 	Country or territory where airport is located;
   <br>e. **IATA**:  3-letter IATA code - **Unused data**;
   <br>f. **ICAO**:  4-letter ICAO code;
   <br>g. **Latitude**: 	Latitutide in decimal degrees. Negative is South, positive is North;
   <br>h. **Longitude** :	Longitude in decimal degrees. Negative is West, positive is East;
   <br>i. **Altitude**: 	Altitude in feet - **Unused data**;
   <br>j. **Timezone**: 	Hours offset from UTC  - **Unused data**;
   <br>k. **DST**: 	Daylight savings time. One of E (Europe), A (US/Canada), S (South America), O (Australia), Z (New Zealand), N (None) or U (Unknown)  - **Unused data**;
   <br>l. **Tz**: Timezone in "tz" (Olson) format, eg. "America/Los_Angeles" - **Unused data**;
   <br>m. **Type**: 	Type of the airport - **Unused data**;
   <br>n. **Source**: 	Source of this data - **Unused data**.
   <br> **Updated: 23/12/2019**
3. Airport Database⁴ with extra data - <a href="/data/processed/AirportExtraData.csv">AirportTestExtraData.csv</a> <a href="https://github.com/tamagusko/ViseuAirportStudy/blob/master/README.md#-references">[3]</a>
   <br>a. **ICAO**:  4-letter ICAO code;
   <br>b. **RWYLenght**:  Runway length in meters;
   <br>c. **PCN**:  Runway structural strength number.
   <br> **Updated: 28/12/2019**  
4. Basemap shapefile - <a href="/data/processed/gis/20191227_basemap.shp">20191227_basemap.shp</a> <a href="https://github.com/tamagusko/ViseuAirportStudy/blob/master/README.md#-references">[4]</a>
   <br>a. Layer file with boundaries of countries;
   <br> **Updated: 28/12/2019**
   
The data is UTF-8 encoded.

<h2>Use:</h2>

**AnalysisByRWY(PCN, RWYLenght)**
> analysisByRWY(PCN, RWYLenght)
<br>Aircraft served: Aircrafts
<br>Routes served: Airports

If you want to change the list of **aircraft** under study, edit the file: **Aircraft database (AircraftData.csv)**
<br>If you would like to change the list of **airports** under study, edit the file: **Airport extra database (AirportExtraData.csv)**

Notes: 

**¹** Indicates, among other elements, the structural strength of the pavement. <br>
**²** It is related to the impact of the aircraft on the pavement, and must be less than or equal to the runway PCN. <br>
**³** Information not required. <br>
**⁴** Shengen area airports only (lower airport security requirements).

<h1>Results of Study:</h1>

![Results 20191229 by Tamagusko](https://github.com/tamagusko/ViseuAirportStudy/blob/master/reports/20191229Results.png)

<a href="/reports/20191229Results.pdf">Download this file in format PDF</a> 

<h1>Future developments</h1>

1. Improve code with L.tooltip and json for leaflet:
<br>a. Change markers for airports;
<br>b. Put interactive labels (ICAO codes) for airports;
<br>c. Show legend with: Reference_Airport and Served_Airports

2. Rebuilding the functions for generic application, example:
<br>a. analysisByRWY(ReferenceAirport,PCN,RWYLenght);
<br><br>This study was not necessary as it is focused only on LPVZ (Viseu Airport).

3. Build/process a database with flight routes to evaluate possible connections.
<br><br>Interesting to see the range that the reference airport can have with a simple connection.

<h1> Citation</h1>
<br>Tamagusko, T. and Ferreira, A. (2020). Data Analysis applied to Airport Pavement Design, Submitted to Proceedings of the 6th International Conference on Road and Rail Infrastructure, Pula, Croatia.
<br>Tamagusko, Tiago. (2020). Airport Pavement Design. https://doi.org/10.13140/RG.2.2.19628.00640

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

<h1> References</h1>
[1] Martins, J. P. F. (2018). Reflexão sobre a viabilidade e localização de uma infraestrutura aeroportuária na região Centro de Portugal (Universidade do Porto). https://doi.org/10.13140/RG.2.2.34944.69124
<br>[2] OpenFlights (2019). Airport, airline and route data. Retrieved December 23, 2019, from https://openflights.org/data.html
<br>[3] World Aero Data (2019). World Aeronautical Database. Retrieved December 28, 2019, from https://worldaerodata.com
<br>[4] Natural Earth (2019). Free vector and raster map data at 1:10m, 1:50m, and 1:110m scales. Retrieved December 25, 2019, from http://www.naturalearthdata.com<br><br>
