# Ferry-Induced Wave Dynamics in the Finnish Archipelago Sea

## Name  
Mariah Josten

## Contact  
Email: mariah.josten@utu.fi  
ORCID: https://orcid.org/0000-0002-8133-8112  

## Organizational Affiliation  
Fluvial and coastal research group, Department of Geography, University of Turku

---

# Project Overview

## Problem Statement

Large passenger ferries regularly transit through the Finnish Archipelago Sea, a complex archipelago characterized by shallow bathymetry, narrow fairways, and wind-driven hydrodynamics. Vessel-induced waves may increase turbidity, resuspend sediment, and alter nearshore flow conditions. However, the combined influence of bathymetry, vessel properties, and meteorological forcing on ship-wave propagation remains poorly constrained in complex coastal environments.

## Challenge Statement

Previous studies on ship-indcued waves have focused on confined waters, such as river and dredged channels. In heterogeneous archipelagic systems, variable bathymetry, wind forcing, and vessel characteristics complicate prediction of wave amplitude and energy. Empirical, spatially distributed in situ observations remain limited in the study area.

## Solution Statement

This project provides new field-based empirical constraints on ferry-induced primary and secondary wave propagation across distance gradients from a major fairway in the Archieplago Sea. It integrates hydrodynamic measurements with AIS vessel data and meteorological observations to quantify the dominant drivers of wave amplitude and energy.

## Research Questions

1. Determine which geospatial, vessel, and meteorological factors most strongly control ferry-induced wave amplitude and energy.  
2. Identify the distance from the fairway at which ferry-induced fluctuations in water level and flow velocity remain detectable.


---

# Literature Context

The analytical framework combines:

- AIS records and linear wave theory for estimating timing of ferry wave events  
- Signal processing techniques (bandpass filtering and envelope detection)  
- Interpretable machine learning approaches for environmental driver ranking
- 
---

# Data Sources

## Field Measurements

- ADCP (flow speed and direction)  
- Pressure transducers (water level)  

## External Datasets

- Wind data from University of Turku Seili weather station (https://saaristomeri.utu.fi/weather/)
- AIS vessel position, course, and speed data (https://globalfishingwatch.org/)

---

# Methods Overview

## Field Campaign Design

High- and low-impact sites are paired to ensure similar geospatial characteristics (depth, slope, exposure, shoreline morphology, and orientation) while differing in distance from the fairway.

## Pressure Data Processing Workflow (Summary)

1. **Data integration and correction**
   - Load site pressure and ADCP data, wind data, and AIS arrival times  
   - Standardize timestamps and site identifiers  
   - Apply atmospheric correction to pressure sensor data  

2. **Signal processing and event detection**
   - Convert corrected pressure to surface elevation  
   - Apply bandpass filtering to isolate ferry-wave frequencies  
   - Use Hilbert envelope and percentile thresholds to detect ferry-induced wave events  
   - Extract time windows around AIS-recorded vessel passages  

3. **Wave metric computation**
   - Calculate wave height, lag time, and potential energy from filtered surface elevation  
   - Process all sites consistently and store event-level results  

## Modeling (In Progress)

Planned modeling approaches include:

- Tree-based ensemble regression to identify dominant drivers of wave amplitude and energy  
- Cross-model comparison to verify robustness of variable importance  
- Classification approaches to estimate the probability of detecting ferry-induced signals with increasing distance from the fairway  

---
# Reproducibility

1. Clone the repository.  
2. Install required packages.  
3. Retreive external and field datsets  
4. Run scripts in order:
   - AIS processing and interpolation
   - Pressure data processing  
   - ML analyses (when finalized)  
---

# Summary of Results

This analysis determines:

- Whether ferry-induced waves are detectable at both high- and low-impact sites  
- Under which environmental and vessel conditions detectability occurs  
- The relative influence of distance, vessel characteristics, bathymetry, and meteorology on primary and secondary wave amplitude and energy  

The results provide quantitative thresholds for spatial extent and environmental modulation of ferry-induced hydrodynamic impacts in complex archipelagic environments.

---

# License

MIT License

---

# Citation

If you use this repository, please cite:

Mariah Josten (2026). *Ferry-Induced Wave Dynamics in the Finnish Archipelago Sea*. GitHub repository. 

---

# Contribution Guidelines

Contributions are welcome via pull requests.

Please:

- Follow the existing directory structure  
- Document new functions  
- Maintain reproducibility  
- Open an issue before proposing major structural changes  


