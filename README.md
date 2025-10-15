# Water Evaporation Monitoring over Maduru Oya Reservoir using VIIRS Data and Python API
## Overview
This project demonstrates a workflow for mapping and monitoring surface water evaporation using the VIIRS (Visible Infrared Imaging Radiometer Suite) evapotranspiration dataset integrated within the Google Earth Engine (GEE) platform and processed through the Python API.

The analysis focuses on the Maduru Oya Reservoir in Sri Lanka, a critical inland water body supporting agriculture and ecosystem balance. Understanding evaporation rates in such reservoirs is essential for water balance assessment, irrigation planning, and climate adaptation in semi-arid regions.

By combining VIIRS-based actual evapotranspiration (ET) data with land cover masking from MODIS, the workflow isolates open-water evaporation dynamics, providing both spatial and temporal insights across multiple years (2015–2025).

## Objectives
1. Estimate monthly and annual evaporation over Maduru Oya Reservoir using VIIRS ET data.
2. Apply land cover masking to isolate evaporation over open-water surfaces (MODIS water class = 17).
3. Generate spatial evaporation maps and annual time-series trends for long-term water resource monitoring.

### Figure 1. Annual Evaporation Maps (2015–2025) - Contour plots showing spatial variations of total annual evaporation over the Maduru Oya Reservoir area.
<img width="1475" height="590" alt="image" src="https://github.com/user-attachments/assets/ad2d940d-ccb3-48d9-8036-f319e69acb5b" />

### Figure 2. Annual Mean Evaporation Trend - A time-series plot displaying year-to-year variations in mean evaporation (mm/year).
<img width="578" height="432" alt="image" src="https://github.com/user-attachments/assets/bfe3122b-f542-466a-985f-862b8a07e04a" />

## Datasets
| Dataset                        | Description                                                           | Source                                     |
| ------------------------------ | --------------------------------------------------------------------- | ------------------------------------------ |
| **VIIRS ET (SSEBop v6)**       | Monthly evapotranspiration product (mm/month) from VIIRS              | `projects/usgs-ssebop/viirs_et_v6_monthly` |
| **MODIS Land Cover (MCD12Q1)** | Yearly global land cover classification; used to extract water pixels | `MODIS/061/MCD12Q1`                        |

## Tools & Libraries
1. Google Earth Engine (GEE) – Satellite data processing and filtering
2. xee – Bridge between Earth Engine and xarray for local data access
3. geemap – Interactive mapping, visualization, and ROI drawing
4. xarray – Handling multi-dimensional time-series data
5. matplotlib – Plotting annual evaporation maps and time-series graphs
6. NumPy – Array operations and handling missing data

## Notes
-  The SSEBop VIIRS ET dataset provides high temporal coverage suitable for water resource studies.
-  MODIS land cover masking ensures evaporation estimates represent open-water surfaces only.
-  The rainbow colormap effectively visualizes evaporation intensity gradients.
-  This workflow can be extended for reservoir operation modeling, evaporation–precipitation balance studies, or climate variability assessments.

## References
1. USGS (2024). VIIRS SSEBop Evapotranspiration v6 Dataset Documentation.
2. MODIS (2023). MCD12Q1 Land Cover Type Product (Collection 6.1).
