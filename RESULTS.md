# 📦 Analysis Results — Heat Wave Dynamics in the Bucharest Region

**DeltaHUB Workshop Project** | Author: **Alexandru Ovedenie** *(Ove)*

---

## Overview

This document provides a reference to all raw outputs generated during the Google Colab analysis pipeline for the **Bucharest Heat Wave Dynamics** project. Results span multiple formats — from georeferenced raster datasets and GIS-ready indicators to final maps and visualizations — and are hosted on Google Drive for full access.

---

## 📂 Results Repository (Google Drive)

All raw outputs produced in Google Colab are publicly accessible at the link below (read-only access):

> 🔗 **[Access the full results folder on Google Drive](https://drive.google.com/drive/folders/1vpMKGBDFg-_jSrnBr7O0AGm1DLUidFsf?usp=sharing)**

The folder is shared in **read-only mode** to preserve the integrity of the original analysis outputs.

---

## 🗂️ Output Types

The results folder contains the following categories of files:

### 🌐 Raster & Climate Data
| Format | Description |
|--------|-------------|
| `.nc` (NetCDF) | Raw and processed climate/meteorological grids (temperature, derived variables) |
| `.zarr` | Chunked array stores for efficient access to large spatio-temporal datasets |
| `.tiff / .tif` (GeoTIFF) | Georeferenced raster outputs ready for GIS software (QGIS, ArcGIS, etc.) |

### 📊 GIS-Ready Indicators
Computed heatwave indices following the **[CLIMPACT methodology](https://climpact-sci.org/indices/)**, exported as spatial data layers compatible with GIS environments:

| Index | Description |
|-------|-------------|
| **HWN** | Heatwave Number — total count of heatwave events per season |
| **HWF** | Heatwave Frequency — number of heatwave days per season |
| **HWD** | Heatwave Duration — length of the longest heatwave event |
| **HWM** | Heatwave Magnitude — mean temperature excess during heatwaves |
| **HWA** | Heatwave Amplitude — peak temperature anomaly during the hottest event |

These indicators are available as `.nc`, `.zarr`, and `.tiff` files for direct use in GIS workflows or further numerical analysis.

### 🗺️ Maps & Visualizations
| Format | Description |
|--------|-------------|
| `.png` | Final cartographic maps and spatial distribution plots of heatwave indicators over the Bucharest region |
| `.png` | Time series plots, trend analyses, and statistical summaries of heatwave dynamics |

---

## 🛠️ How to Use the Data

### In GIS Software (QGIS / ArcGIS)
- Load `.tiff` files directly as raster layers
- Use `.nc` files via the GDAL/NetCDF driver or the built-in NetCDF import tool
- Coordinate Reference System (CRS): check each file's metadata — outputs are georeferenced

### In Python (Google Colab / Jupyter)
```python
import xarray as xr
import rioxarray

# Load NetCDF
ds = xr.open_dataset("your_file.nc")

# Load GeoTIFF
da = rioxarray.open_rasterio("your_file.tiff")

# Load Zarr
ds_zarr = xr.open_zarr("your_store.zarr")
```

### Viewing Maps
`.png` files can be opened directly in any image viewer or embedded in reports and presentations.

---

## 🔗 Related Files in This Repository

| File | Description |
|------|-------------|
| [`Bucharest_Heatwave_Analysis.ipynb`](./Bucharest_Heatwave_Analysis.ipynb) | Full Google Colab notebook — all code, analysis steps, and inline visualizations |
| [`Heatwave_Dinamic_Report.docx`](./Heatwave_Dinamic_Report.docx) | Detailed written report summarizing methodology and key findings |
| [`DATA.md`](./DATA.md) | Information about the input datasets used |
| [`heatwave_analysis_prompt.md`](./heatwave_analysis_prompt.md) | AI prompt used to guide the analytical workflow |

---

## 📄 License & Usage

Results are shared for **educational and research purposes** as part of the DeltaHUB Workshop. Please contact the author before reusing or redistributing any outputs.

---

*Generated as part of the DeltaHUB Workshop — May 2025.*
