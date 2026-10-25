# Spatial Risk Assessment of Urban Sprawl and Wetland Degradation in Low-Lying Lagos (2000–2025)

<p align="center">
  <img src="assets/lagos_spatial_risk_assessment_map.jpg" alt="Spatial Risk Assessment Map of Lagos State" width="100%">
</p>

## Overview
Rapid, unchecked urban expansion across Lagos State is increasingly encroaching upon low-lying floodplains and natural wetland buffers below 5 metres in elevation. This land-use transformation severely disrupts natural drainage pathways and degrades critical coastal ecosystems, dramatically amplifying the region's vulnerability to pluvial and coastal flooding.

This project integrates Earth Observation (EO) data and Geographic Information Systems (GIS) to identify critical spatial collision hotspots where 2000–2025 urban expansion directly overlaps with historical wetland baselines and low-lying elevation zones (≤5 m) across Lagos State.

---

## Key Spatial Findings

| Land Cover / Risk Class | Area ($\text{km}^2$) | Area Share (%) | Description & Risk Implication |
|---|---|---|---|
| **Low-Lying Zones ($\le 5\,\text{m}$)** | $1,671\,\text{km}^2$ | 49.0% | Inherent flood-prone baseline terrain across Lagos State. |
| **Historical Wetlands (1984–2000)** | $784\,\text{km}^2$ | 23.0% | Baseline natural water and wetland retention buffers. |
| **Urban Built-Up (2025)** | $930\,\text{km}^2$ | 27.0% | Extent of urban footprint after 25 years of expansion. |
| **Collision Hotspots** | **$5.6\,\text{km}^2$** | **0.17%** | Acute direct overlap where human development has built over low-lying historical wetlands. |

### Core Insights
* **Extensive Hazard Footprint:** Low-lying zones under 5 metres account for **49% ($1,671\,\text{km}^2$)** of the total land area in Lagos State, creating an inherently flood-prone foundation.
* **Aggressive Expansion:** Built-up urban areas grew to cover **27% ($930\,\text{km}^2$)** of the state by 2025, with significant growth encroaching along vulnerable lagoon corridors.
* **Acute Collision Zones:** **$5.6\,\text{km}^2$ ($0.17\%$)** represents direct, critical collision hotspots where modern infrastructure severely obstructs historic natural drainage baselines.

---

## Data Sources & Tools

### Datasets
* **Elevation & Topography ($\le 5\,\text{m}$):** NASA SRTM / Digital Elevation Model (DEM) via Google Earth Engine & QGIS.
* **Historical Water Baseline (1984–2000):** JRC Global Surface Water Dataset via Google Earth Engine.
* **Urban Built-Up Dynamics (2000–2025):** Multi-temporal satellite imagery (Landsat Surface Reflectance / ESA WorldCover) via Google Earth Engine.
* **Infrastructure & Basemap:** OpenStreetMap (OSM) highway vector layers and basemap tiles.

### Tech Stack
* **Google Earth Engine (GEE):** Cloud-based multi-temporal data extraction, clipping, and classification.
* **QGIS:** Topographic thresholding, spatial raster intersection, cartographic layout design, coordinate annotation (EPSG:4326), and spatial vector overlay.
* **Microsoft Excel:** Statistical aggregation, area percentage calculations ($\text{km}^2$), and summary chart generation.

---

## Methodology & Spatial Workflow

1. **Data Extraction & Boundary Clipping:** Multi-temporal built-up rasters and JRC historical surface water baselines were extracted and clipped to the official Lagos State administrative boundary using GEE scripts.
2. **Elevation Thresholding:** Topographic rasters (NASA SRTM) were filtered in QGIS to isolate all terrain falling below 5 metres above sea level.
3. **Raster Intersection Analysis:** Executed a boolean spatial intersection query in QGIS Raster Calculator:
   $$\text{Collision Hotspots} = (\text{Elevation} \le 5\text{m}) \cap (\text{Historical Wetland}) \cap (\text{Built-Up } 2025)$$
4. **Area Quantification & Cartography:** Exported pixel class statistics to Excel for metric summaries, followed by layout composition in QGIS featuring coordinate grids, inset contextual maps, scale bars, and dynamic legends.

---

## Project Structure

```text
├── assets/
│   └── lagos_spatial_risk_assessment_map.jpg   # Final high-resolution map layout
├── data/
│   ├── raw/                                    # Raw GEE rasters and SRTM DEMs
│   └── processed/                              # Filtered layers and collision rasters
├── scripts/
│   ├── gee_data_extraction.js                  # GEE script for Landsat & JRC extraction
│   └── raster_intersection.py                  # QGIS Python/PyQGIS processing script
├── docs/
│   └── Lagos_Flood_Mapping_Submission_Summary.pdf # Detailed project summary
└── README.md
