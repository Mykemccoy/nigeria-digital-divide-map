# Mapping Nigeria's Digital Divide Through Geospatial Data
### State-Level Synthesis of Broadband Performance, Spatial Statistics, and Digital Equity Priorities

<div align="center">

[![Live Interactive Map](https://img.shields.io/badge/🌍_Live_Interactive_Map-Explore_Atlas-blue?style=for-the-badge)](https://mykemccoy.github.io/nigeria-digital-divide-map/#6/13.154/6.471)
[![QGIS](https://img.shields.io/badge/Powered_by-QGIS_%7C_Leaflet-green?style=for-the-badge)](https://qgis.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

</div>

---

## 👥 Authors (TEAM MAACs)
* **Ayewa Olanrewaju Michael**
* **Clinton Hickson Eyyammeh** 
* **Owolabi Abdulquawiyy Adisa** 
* **Awwal Abdulwahab**

---

## 🗺️ Project Overview
This project uses the Ookla internet performance dataset and supporting population and socioeconomic data to examine how internet performance varies across Nigeria. The aim is to identify states where weak observed connectivity overlaps with population exposure or socioeconomic need, while distinguishing areas with poor performance from areas where the available data are limited. The results provide a spatial basis for deciding where further connectivity assessment and investment should be considered.

---

## 📊 Executive Synthesis Map Atlas
The maps synthesize state-level internet download speeds, spatial hotspots, and socioeconomic data into a unified **Digital Equity Priority Index (DEPI)** to guide broadband infrastructure investment across Nigeria.


---

## MAPPING NIGERIA'S DIGITAL DIVIDE THROUGH GEOSPATIAL DATA

<p align="center">
  <img src="LAGOS SPATIAL RISK ASSESSMENT MAP.png" alt="Spatial Risk Assessment Map of Urban Sprawl and Wetland Degradation in Low-Lying Lagos (2000-2025)" width="850"/>
</p>

LAGOS SPATIAL RISK ASSESSMENT MAP.png
---


![Mapping Nigeria's Digital Divide Through Geospatial Data](Assessment%20of%20Broadband%20Performance%20(TEAM%20MAACs).pdf) <!-- Alternatively, if your image is saved in the repo as an image file like assets/map.png, use: ![Synthesis Map](assets/map.png) -->

> **Figure 1:** State-level synthesis of download speed, spatial hotspot values, population exposure, digital equity priority, and data coverage.

---

## 🌐 Interactive Web Dashboard
Explore the live, interactive multi-layer web application:
🔗 **[Access the Live Interactive Map Here](https://mykemccoy.github.io/nigeria-digital-divide-map/#6/13.154/6.471)**[cite: 11]

* **Multi-Layer Toggle:** Switch seamlessly between State and Local Government level layers.
* **Advanced Search:** Use the search utility to locate precise states or LGAs instantly.
* **Dynamic Popups:** Click or hover over any region to inspect download speeds, upload rates, latency, observation counts, population, priority class, and data-quality status.

---

## 🔍 Key Findings from the Map
* **Significant Regional Disparity:** Connectivity varies significantly by location. The download-speed map shows a mix of severe- and moderate-deficit classes across several states, while higher-speed classes are found in fewer areas. Consequently, a national average would obscure important regional differences.
* **Multidimensional Need:** Need cannot be assessed by download speed alone. The population-exposure layer distinguishes areas where high connectivity deficits coincide with large populations from those where they overlap with high poverty levels, supporting a comprehensive assessment of vulnerability.
* **Data Availability & Measurement Silence:** Ookla observations are unevenly distributed across states, so areas with limited coverage should be prioritized for additional data collection rather than interpreted as locations without internet service.

---

## ⚙️ Spatial Assessment & Methodology
The state-level maps compare download speed, display the spatial statistic used for hotspot analysis ($Gi^*$), group population exposure, rank digital equity priorities, and show the distribution of data coverage. 

The **Digital Equity Priority Index (DEPI)** combines connectivity deficit (50%), population (30%), and poverty (20%) after inputs are normalized on a common 0–100 scale. Hotspot results should be interpreted as statistically significant only where the relevant $Gi^*$ significance test supports that conclusion.

---

## 💡 Recommended Actions
1. **Validate Priority Areas:** Cross-check states in the highest DEPI class with current coverage information, operator data, and local evidence before selecting locations for intervention.
2. **Investigate Overlapping Need:** Give focused attention to areas where poor observed speeds coincide with high population exposure or poverty, rather than allocating resources based on download speed alone.
3. **Improve Evidence in Data-Poor Areas:** Review states with limited Ookla observations and seek additional operator, regulator, or field data before drawing conclusions about service quality.
4. **Use Results for Strategic Planning:** Assess feasible options such as network upgrades, additional backhaul, new infrastructure, or shared-access facilities only after local coverage, demand, and cost checks.

---

## ⚠️ Deliverables and Limitations
The primary output is a state-level synthesis map supported by underlying download-speed, hotspot, population-exposure, DEPI, and data-coverage layers. 

The analysis is observational and subject to several limitations: Ookla speed tests may not represent every resident or network, population and poverty datasets may differ in reference year and spatial resolution, and state-level summaries may conceal internal local variations. Furthermore, Ookla data were unavailable for more than one-third of Nigeria's local government areas, which limited deep in-depth assessment at the LGA level.
