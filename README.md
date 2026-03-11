# Environmental Change-Detection-Workflow-
This repository demonstrate my geospatial analytical skills such as API based data download, geospatial analysis and change detection
# 🌊 Automated Flood Inundation Mapping (SAR + Optical Fusion)

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue)](https://www.python.org/)
[![Status](https://img.shields.io/badge/Status-Prototype-orange)]()
[![License](https://img.shields.io/badge/License-MIT-green)]()

## 📌 Overview
This repository contains an end-to-end geospatial pipeline for **Rapid Flood Assessment**. It integrates **Sentinel-1 (SAR)** and **Sentinel-2 (Optical)** satellite imagery to detect floodwaters, overcoming the limitations of optical sensors during cloud-heavy monsoon events.

The system performs automated data ingestion, pre-processing (speckle filtering), change detection (using Otsu's thresholding and NDWI), and generates a professional PDF report for stakeholders.

## 🚀 Key Features
* **Multi-Sensor Fusion:** Combines the all-weather capability of SAR with the contextual clarity of Optical data.
* **Robust Pre-processing:** Implements Median Blur and Normalization to handle SAR speckle noise.
* **Automated Thresholding:** Uses Otsu’s Binarization for dynamic water extraction (no manual threshold tuning required).
* **Noise Removal:** Morphological area filtering to eliminate false positives (small puddles/noise < 2 hectares).
* **Automated Reporting:** Generates a publication-ready PDF report containing maps, statistics, and error analysis.

## 🛠️ Tech Stack
* **Core Logic:** Python, NumPy
* **Geospatial Processing:** Rasterio, GeoPandas (for shapefile/AOI handling),opencv
* **Data Access:** SentinelSat / ASF Data_Search
* **Visualization:** Matplotlib


## 📂 Project Structure
```bash
├── data/
│   ├── sentinel 1 and sentinel 2/               # Raw Sentinel-1 (VV/VH) and Sentinel-2 (.tif)
│   ├── processed /                              # Processed tiffs
├── src/
│   ├── download_data.ipynb     # Script to fetch data from Copernicus/ASF
│   ├── preprocess.ipynb        # Preprocessing logic
│   ├── analysis.py              # Main change detection algorithm (Otsu/NDWI)
│   
├── notebooks/               # Jupyter notebooks for exploratory analysis
├── requirements.txt         # Dependencies
└── README.md
