# Time-Series Analysis using CCDC Equation

## Overview
This project is a part of the Master of Technology thesis by Rochitansh Singh at the Department of Mathematics, Indian Institute of Technology Madras. The project focuses on determining the variety of Potato crops using Time Series Analysis and NDVI Index by implementing the CCDC Equation.

## Table of Contents
- [Introduction](#introduction)
- [Variety of Potatoes](#variety-of-potatoes)
- [Implementation](#implementation)
- [Data and Processing](#data-and-processing)
- [Results and Conclusions](#results-and-conclusions)
- [References](#references)

## Introduction
Geographic information can be represented in the form of paper maps or digital formats. The process of detecting alterations in the status of an object or phenomenon is known as change detection. This project employs a new algorithm for continuous change detection and classification (CCDC) of land cover using all available Landsat data. The aim is to identify the variety of potato crops provided the Sowing Date and Harvesting Date.

## Variety of Potatoes
This section provides information about different varieties of potatoes used in the project:
1. **Sanatana Plain**: Used for making chips and fries.
2. **Bafana Potatoes**: Fully mature in 115-120 days.
3. **Kennebac Potatoes**: Medium to large, available year-round.
4. **Kufri Frysona**: Suitable for French fry production, high field resistance to late blight disease.
5. **Innovator Potato**: Popular for frying and baking.
6. **Sarpo Mira**: Vigorous growth, high yield potential.
7. **Santana Potato**: Used for boiling, baking, and chipping.

## Implementation
### CCDC Equation
The CCDC algorithm employs all cloud-masked Landsat surface reflectance data to track various types of land change. It does not filter changes based on specific spectral directional changes, nor does it rely on a single spectral band or index.

### NDVI Value
NDVI (Normalized Difference Vegetation Index) measures the difference between near-infrared and red light to quantify vegetation. The NDVI value ranges from -1 to +1, indicating different types of land cover.

### Analysis Ready Data
The USGS creates Landsat ARD for the CONUS using imagery from the Landsat 4 and 5 TM, Landsat 7 ETM+, and Landsat 8 OLI. These data are pre-processed for time series analysis.

## Data and Processing
### Dataset
The dataset is provided by Cropin Technologies and consists of different species of Potato crops, their sowing and harvesting dates, and NDVI values. The dimensions of the dataset are 223719 x 33.

### Processing
The CCDC equation is implemented to calculate the fixed number of coefficients for each time series data. The NDVI values over time are analyzed to determine the variety of potato crops.

## Results and Conclusions
### Results
The Random Forest classifier was applied, achieving an accuracy of 31.3%. This result indicates that the CCDC algorithm effectively predicts the variety of unseen data.

### Conclusions
Representing time series as a fixed set of coefficients of the CCDC equation is a better way of representing and processing data than working with time series of various lengths.

## References
1. Zhu, Z., & Woodcock, C. E. (2014). Continuous change detection and classification of land cover using all available Landsat data. Remote Sensing of Environment, 144, 152-171. [DOI:10.1016/j.rse.2014.01.011](https://doi.org/10.1016/j.rse.2014.01.011)
2. Coppin, P. R., & Bauer, M. E. (1996). Digital change detection in forest ecosystems with remote sensing imagery. Remote Sensing Reviews, 13(3-4), 207-234.
3. Brown, J., et al. (2019). Lessons learned implementing an operational continuous United States national land change monitoring capability: The Land Change Monitoring, Assessment, and Project (LCMAP) approach. Remote Sensing of Environment, 238. [DOI:10.1016/j.rse.2019.111356](https://doi.org/10.1016/j.rse.2019.111356)
