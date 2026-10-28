# Spatial Risk Assessment of Urban Sprawl and Wetland Degradation in Low-Lying Lagos (2000–2025)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Google Earth Engine](https://img.shields.io/badge/Google%20Earth%20Engine-Spatial%20Analysis-green.svg)](https://earthengine.google.com/)
[![QGIS](https://img.shields.io/badge/QGIS-v3.x-blue.svg)](https://qgis.org/)

## Project Summary
Rapid, unchecked urban expansion across Lagos State is increasingly encroaching upon low-lying floodplains and natural wetland buffers below 5 metres in elevation. This land-use transformation severely disrupts natural drainage pathways and degrades critical coastal ecosystems, dramatically amplifying the region's vulnerability to pluvial and coastal flooding.

Using multi-temporal satellite classification (Landsat Surface Reflectance / ESA WorldCover) and JRC Global Surface Water baselines in Google Earth Engine alongside NASA SRTM topographic elevation rasters and OpenStreetMap vectors in QGIS, this study evaluates spatial collision hotspots where 2000–2025 urban expansion directly overlaps with historical wetland baselines and low-lying elevation zones (≤ 5m) across Lagos State.

---

## SPATIAL RISK ASSESSMENT MAP

<p align="center">
  <img src="LAGOS SPATIAL RISK ASSESSMENT MAP.png" alt="Spatial Risk Assessment Map of Urban Sprawl and Wetland Degradation in Low-Lying Lagos (2000-2025)" width="850"/>
</p>

---

## Key Spatial Findings

| Class / Land Cover Category | Area (km²) | Area Share (%) | Description & Risk Implication |
|---|---|---|---|
| **Low_Lying Zones (≤ 5m)** | 1,671 | 49% | Inherently flood-prone terrain foundation under 5m elevation. |
| **Historical Wetland (1984–2000)** | 784 | 23% | Natural water baselines and wetland buffers. |
| **Urban Built Up (2025)** | 930 | 27% | Extent of urban footprint expanded along vulnerable lagoon corridors. |
| **Collision Hotspots** | **5.6** | **0.17%** | Acute direct collision hotspots where human development built over low-lying historical wetlands. |

### Core Insights
* **Extensive Hazard Footprint:** Low-lying zones under 5 metres account for **49% (1,671 km²)** of the total land area in Lagos State, creating an inherently flood-prone foundation[cite: 3].
* **Aggressive Expansion:** Built-up urban areas grew to cover **27% (930 km²)** of the state by 2025, with significant growth encroaching along vulnerable lagoon corridors[cite: 3].
* **Critical Collision Zones:** **5.6 km² (0.17%)** represents acute direct collision hotspots where human development has completely built over low-lying historical wetlands[cite: 3].

---

## Methodology
The methodology combines cloud-based multi-temporal remote sensing extraction with terrain thresholding and spatial raster calculator analysis:

```mermaid
graph TD;
    A[NASA SRTM DEM / Topography] --> B[Elevation Thresholding in QGIS: Elevation <= 5m];
    C[JRC Global Surface Water 1984-2000] --> D[Extract Historical Wetland Baseline in GEE];
    E[Landsat / ESA WorldCover 2000-2025] --> F[Multi-Temporal Built-Up Classification in GEE];
    B --> G[Raster Intersection Analysis in QGIS Raster Calculator];
    D --> G;
    F --> G;
    G --> H[High-Risk Collision Hotspot Extraction];
    H --> I[Class Area Quantification & Percentage Summaries in Excel];

