# Design of the Viseu Aerodrome Runway

Final project developed in the Informatics, Systems and Programming discipline of the Master in Geographic Information Technologies of the University of Coimbra, taught by Dr. Alberto Jorge Lebre Cardoso in the academic year 2018-2019.

## Basic info

[![Open Source? Yes!](https://badgen.net/badge/Open%20Source%20%3F/Yes%21/blue?icon=github)](https://github.com/tamagusko) [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE.md) [![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/) 

© Tiago Tamagusko (tamagusko@gmail.com) - [tamagusko.github.io](https://tamagusko.github.io)  
 Version: 0.6.1 (2022/01/12)  
 Required libraries: [requirements](/requirements.txt)  
 Project Page: [github.com/tamagusko/ViseuAirportStudy](https://github.com/tamagusko/ViseuAirportStudy/)  

## Problem

Viseu Aerodrome is interested in servicing bigger aircraft, which enable longer range and carry more passengers per aircraft [[1]](#1). This requires improving the structural strength of the pavement and increasing the length of its runway.

## Proposal

In order to design an airport pavement, it is necessary to know two main characteristics, namely the Pavement Classification Number¹ (PCN) and the extension of the runway.

Thus, the proposed challenge is to design a pavement with capacity (PCN) and extension to meet a desired group of routes.

## Project data structure:

    ├── preprocessing.ipynb            # Preprocessing 
    ├── analysis.ipynb                 # Data analysis
    ├── TODO.md                        # Future developments
    ├── data                  
    │          ├── raw                 # Raw data
    │          ├── processed           # Data processed
    ├── reports                        # Outputs

## Shortcuts:

1. [Preprocessing](preprocessing.ipynb)  
2. [Data analysis](analysis.ipynb)
3. [Future developments](TODO.md)
4. [Data information](/data)

## Use:

**AnalysisByRWY(PCN, RWYLenght)**

> analysisByRWY(PCN, RWYLenght)  
> Aircraft served: Aircrafts  
> Routes served: Airports

```
Changes:

To change the aircrafts, edit the file: 
AircraftData.csv

To change the airports, edit the file: 
AirportExtraData.csv

Notes:

1. Indicates, among other elements, the structural strength of the pavement.  
2. It is related to the impact of the aircraft on the pavement, and must be less than or equal to the runway PCN.  
3. Information not required.  
4. Shengen area airports only (lower airport security requirements).
```

# Results of Study:

[Download this file in format PDF](/reports/20191229Results.pdf)

# Citation

Tamagusko, T. (2020). Airport Pavement Design. https://doi.org/10.13140/RG.2.2.19628.00640

```bibtex
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

[1] 
Martins, J. P. F. (2018). 
Reflexão sobre a viabilidade e localização de uma infraestrutura aeroportuária na região Centro de Portugal (Universidade do Porto). https://doi.org/10.13140/RG.2.2.34944.69124
