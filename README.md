# Viseu Aerodrome Runway Study

Project[^1] that calculates served airports and accepted aircraft based on runway characteristics.

## Basic info

© Tiago Tamagusko (tamagusko@gmail.com) - [tamagusko.github.io](https://tamagusko.github.io)   
Required libraries: [requirements](/requirements.txt)  

## Problem

Viseu Aerodrome is interested in servicing bigger aircraft, which enable longer range and carry more passengers per aircraft [(Martins, 2018)](#references). This requires improving the structural strength of the pavement and increasing the length of its runway.

## Proposal

In order to design an airport pavement, it is necessary to know two main characteristics, namely the Pavement Classification Number[^2] (PCN) and the extension[^3] of the runway.

Thus, the proposed challenge is to design a pavement with capacity (PCN) and extension to meet a desired group of routes[^4].

[^1]: Developed for the discipline of Informatics, Systems and Programming (Prof. Alberto Cardoso) at the University of Coimbra, academic year 2018-2019.
[^2]: Indicates, among other elements, the structural strength of the pavement.
[^3]: Aircraft need a minimum runway length to land.
[^4]: Schengen area only, to ease security issues.

## Project data structure

    ├── preprocessing.ipynb            # Preprocessing 
    ├── analysis.ipynb                 # Data analysis
    ├── data                  
    │          ├── raw                 # Raw data
    │          ├── processed           # Data processed
    ├── reports                        # Outputs

## Shortcuts

1. [Preprocessing](preprocessing.ipynb)  
2. [Data analysis](analysis.ipynb)
3. [Data information](/data)
4. [Future developments](TODO.md)

## Use

In the analysis.ipynb notebook, run:

**AnalysisByRWY(PCN, RWYLenght)**

Output:

> Aircraft served: Aircrafts  
> Routes served: Airports

# Results

![](/reports/20191229Results.png)
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

Martins, J. P. F. (2018). 
**Reflexão sobre a viabilidade e localização de uma infraestrutura aeroportuária na região Centro de Portugal** (Universidade do Porto). https://doi.org/10.13140/RG.2.2.34944.69124
