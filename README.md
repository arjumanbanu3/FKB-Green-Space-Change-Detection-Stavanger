# Public Green Space Changes in Stavanger Municipality (2024–2026)

## Overview

This project investigates changes in publicly mapped green areas in Stavanger Municipality between 2024 and 2026 using official FKB (Felles Kartdatabase) datasets from Geonorge.

A temporal GIS workflow was developed in QGIS to identify, quantify, and visualize areas where public green-space polygons changed between the two datasets.

---

## Objectives

- Compare public green areas from 2024 and 2026.
- Detect spatial changes in mapped green-space extent.
- Quantify significant change areas.
- Produce municipality-wide and site-specific change maps.

---

## Study Area

**Stavanger Municipality, Norway**

The analysis focuses on public green-space datasets clipped to the Stavanger municipal boundary.

---

## Data Sources

### Geonorge

Official Norwegian spatial data portal:

https://kartkatalog.geonorge.no/metadata/parker-og-turomraader-wfs/7c791cc8-567c-49ad-97b7-38776a107dc5?search=FKB%20%20WFS 

### Datasets

- FKB Public Green Areas 2024 (Offentlige grøntområder 2024)
- FKB Public Green Areas 2026 (Offentlige grøntområder 2026)
- Stavanger Municipality Boundary

### Access Method

- Geonorge WFS (Web Feature Service)
- Data accessed directly in QGIS

---

## Software Used

- QGIS
- Geonorge WFS
- Basemap (Topografisk norgeskart and Google Satellite)
- Norway in Pictures (for visual reference where applicable)

---

## Methodology

### 1. Data Collection

- Connected to Geonorge WFS services.
- Loaded FKB Public Green Area datasets for 2024 and 2026.

### 2. Data Preparation

- Clipped both datasets to Stavanger Municipality.
- Checked geometry and attribute consistency.

### 3. Change Detection

A Symmetrical Difference analysis was performed with:

Input Layer:
Offentlige grøntområder 2026

Overlay Layer:
Offentlige grøntområder 2024

This identified areas present in one dataset but not the other.

### 4. Area Calculation

Polygon areas were calculated using:

```
$area
```

and stored in a field named:

```
Area_m2
```

### 5. Filtering Significant Changes

Only polygons larger than:

```
5000 m²
```

were retained for detailed investigation and mapping.

### 6. Classification

Detected changes were separated into:

- Areas Present in 2024 Only
- Areas Present in 2026 Only

---

## Results

### Key Findings

- Initial change polygons detected: 1,737
- Significant changes retained for interpretation: 56
- Largest detected change: 36,482 m² (3.65 ha)
- Largest change area located near Revheim, Stavanger

The analysis identified both:

- Areas present only in the 2024 dataset
- Areas present only in the 2026 dataset

Visual inspection indicated that some changes represent updates to polygon delineation, while others represent substantial changes in mapped public green-space extent.

---

## Maps Produced

### Figure 1

Public Green Space Changes in Stavanger Municipality (2024–2026)

<img width="1851" height="1316" alt="image" src="https://github.com/user-attachments/assets/c061992c-3ac7-4e7a-8b01-d2cd702ab95a" />


This map presents all significant green-space changes detected across Stavanger Municipality.

### Figure 2

Largest Detected Public Green Space Change near Revheim


<img width="1840" height="1306" alt="image" src="https://github.com/user-attachments/assets/1933e7b1-137b-4a28-85fa-f35b02891ad9" />

This case-study map highlights the largest detected change polygon (36,482 m²).

---

## Skills Demonstrated

- GIS Data Acquisition
- Geonorge WFS Integration
- FKB Dataset Management
- Spatial Data Processing
- Change Detection Analysis
- Symmetrical Difference Analysis
- Area Calculation and Statistics
- Cartographic Design
- Municipal GIS Workflows
- QGIS

---

## Project Significance

This project demonstrates how official Norwegian FKB datasets can be used to monitor changes in public green spaces through time. The workflow provides a practical example of municipal-scale GIS analysis and spatial change detection using openly available geospatial data.

---

## Author

Arjuman Banu

MSc in Environmental Engineering

GIS | Spatial Analysis | QGIS | Python
