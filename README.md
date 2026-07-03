## Overview

This project was created as part of my first university course using QGIS independently. The aim was to become familiar with the complete GIS workflow, including data acquisition, preprocessing, spatial analysis and map creation.

The objective of the project was to identify suitable residential areas in Baden-Württemberg based on two personal criteria:
- within 6 km of a larger city (with minimum area of 17 m² -> Friedrichshafen as reference)
- within 1 km of a forest (with minimum area of 0.8 m²)

The analysis was carried out using openly available geospatial datasets and QGIS.

---

## Workflow

- Download and prepare land use datasets
- Merge and preprocess vector layers
- Create buffer zones around cities and forests
- Apply spatial overlay operations (Clip, Dissolve, Intersection, Difference)
- Build a QGIS Model to automate repetitive processing steps
- Visualize the final suitability map

---

## Software

- QGIS 3.40
- Open GeoData Baden-Württemberg
- QuickMapServices (Bing Satellite)

---

## Challenges

During the project, several challenges had to be addressed:

- The original land use data consisted of many separate polygons, requiring extensive preprocessing before analysis.
- Urban areas had to be merged using buffer and dissolve operations. There was no initial polygon layer for city areas itself, so I had to create them by myself. Therefore I buffered all urban land use categories (residential use, public facilities, commercial services, ...). Choosing a suitable buffer zone required several attempts because roads and rivers had to be crossed.
- Comparing calculated urban areas with official city sizes revealed differences caused by the underlying land-use data rather than administrative boundaries (calculated area of Friedrichshafen: 17 m², official: 69 m²).
- Some smaller villages/administrative independent towns were sometimes mixed up
- Processing the complete dataset for Baden-Württemberg was computationally demanding, so the analysis was performed separately for each administrative district before merging the results.

## Results

The analysis identified approximately **10.8%** of the area of Baden-Württemberg as potentially suitable according to the selected criteria.

The project also demonstrated how GIS can support spatial decision-making by combining multiple datasets into a reproducible workflow.

---

## What I learned

This project was my first independent GIS project and provided hands-on experience with:

- vector data processing
- spatial analysis
- buffering and overlay operations
- data preprocessing
- building automated workflows with the QGIS Model Builder
- creating reproducible GIS analyses
