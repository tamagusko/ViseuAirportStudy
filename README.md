<h1>Design of the Viseu Aerodrome runway</h1>

©Tiago Tamagusko (tamagusko@gmail.com). 
<br> Version: 0.2 (22/12/2019)
<br> Using: Python 3, UTF-8, PEP 8
<br> Required libraries: pandas, numpy, matplotlib, seaborn, geopandas, geopy.
<br> Project Page: <a href="https://github.com/tamagusko/ViseuAirportStudy/">github.com/tamagusko/ViseuAirportStudy</a>
<br> Licence: Apache-2.0, see <a href="/LICENSE.md">LICENSE.md</a> for more details.


<h2>Problem</h2>

The Viseu Aerodrome is interested in serving larger aircraft with longer range and number of seats [1]. This requires improving the structural strength of the pavement and increasing the length of its runway.

<h2>Proposal</h2>

In order to design an airport pavement, it is necessary to know two characteristics, namely the Pavement Classification Number¹ (PCN) and the extension of the runway.

Thus, the proposed challenge is to design a pavement with capacity (PCN) and extension to meet a desired group of routes.

<h2>Project data structure</h2>
    
    ├── 1-preprocessing.ipyng    # Database preprocessing 
    ├── 2-analysis.ipynb               # Data analysis
    ├── data                  
    │          ├── raw                       # Raw data
    │          ├── processed           # Data processed
    ├── reports                              # Outputs
    
<h2>Input data</h2>

1. Aircraft database - <a href="/data/processed/AircraftTestData.csv">AircraftTestData.csv</a> 
   <br>a. **Aircraft**: Aircraft identification;
   <br>b. **ACN**²: Aircraft Classification Number;
   <br>c. **RequiredExtension**: Runway length required for landing and takeoff operations;
   <br>d. **Autonomy**: Aircraft autonomy;
   <br>e. **Passagers**³: Number of passengers carried.

2. Airport database  - <a href="/data/processed/AirportTestData.csv">AirportTestData.csv</a>  [2]
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
3. Airport Database with extra data - <a href="/data/processed/AirportTestData.csv">AirportTestExtraData.csv</a>
   <br>a. **ICAO**:  4-letter ICAO code;
   <br>a. **RWYLenght**:  Runway length in meters;
   <br>a. **PCN**:  Runway structural strength number.
   
The data is UTF-8 encoded.

<h2>Results</h2>

**AnalysisByRoutes(AirportsICAOCodes)**
> AnalysisByRoutes(ICAO1,ICAO2,ICAO3)
<br>Required runway PCN: *Value*
<br>Required runway lenght: *Value (m)*
<br>Aircraft served: *Aircrafts*

**AnalysisByRunway(PCN, RWYLenght)**
> AnalysisByRunway(PCN, RWYLenght)
<br>Aircraft served: Aircrafts
<br>Routes served: Airports

**AnalysisByDistance(Distance)**
> AnalysisByDistance(Distance)
<br>Required runway PCN: Value
<br>Required runway lenght: Value (m)
<br>Aircraft served: Aircrafts
<br>Routes served: Airports


Notes: 

**¹** Indicates, among other elements, the structural strength of the pavement. <br>
**²** It is related to the impact of the aircraft on the pavement, and must be less than or equal to the runway PCN. <br>
**³** Information not required.


<h1> References (Corrigir)</h1> 
[1] Martins, J. (2018).  Reflexãoo sobre a viabilidade e localização de uma infraestrutura aeroportuária na região Centro de Portugal. Doi: 10.13140/RG.2.2.34944.69124.
<br>[2] https://openflights.org/data.html. Acessed in December 20, 2019<br><br>

# Project under development
