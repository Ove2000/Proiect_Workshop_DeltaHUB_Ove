# Raw Data — Access & Replication

This file documents the source of the meteorological data used in the analysis and provides the necessary instructions for accessing and replicating the results.

---

## Data Source

The `.nc` (NetCDF) files used in this analysis are sourced from the Romanian Government's open data portal:

**Daily Gridded Meteorological Data**
🔗 [https://data.gov.ro/dataset/date-meteorologice-zilnice-gridate](https://data.gov.ro/dataset/date-meteorologice-zilnice-gridate)

The data are publicly available through [data.gov.ro](https://data.gov.ro) and can be downloaded directly from the link above.

---

## Dataset Description

| Property | Details |
|---|---|
| **Format** | NetCDF (`.nc`) |
| **Temporal coverage** | 1961 – 2025 |
| **Variable** | Daily maximum air temperature at 2 m height (TX) |
| **Spatial resolution** | 1 km × 1 km |
| **Temporal resolution** | 1 day (voxel size: 1 km × 1 km × 1 day) |
| **Method** | Spatial interpolation of observations collected from Romanian meteorological stations, aggregated as daily means |
| **Producer** | Alexandru Dumitrescu — National Meteorological Administration of Romania (ANM) |
| **Contact** | [dumitrescu@meteoromania.ro](mailto:dumitrescu@meteoromania.ro) |

---

## Replicating the Analysis

To replicate the analysis, follow the steps below:

1. **Download the raw data** from the link above.
2. **Place the `.nc` files** in the appropriate directory within the repo (e.g., `data/raw/`).
3. **Run the analysis scripts** in the order indicated in the documentation / notebooks.

> **Note:** Make sure you have the necessary libraries installed for reading NetCDF files (e.g., `xarray`, `netCDF4`, `cfgrib` for Python).

---

## Citation

If you use these data in your work, please cite the original source according to the terms indicated on [data.gov.ro](https://data.gov.ro/dataset/date-meteorologice-zilnice-gridate).
