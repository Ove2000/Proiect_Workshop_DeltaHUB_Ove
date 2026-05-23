# 🌡️ Heat Wave Dynamics in the Bucharest Region

**DeltaHUB Workshop Project** | Author: **Alexandru Ovedenie** *(aka Ove)*

---

## 📌 Overview

This project was developed as part of a **DeltaHUB Workshop**, with the goal of analyzing and understanding the dynamics of **heat wave phenomena in the Bucharest region**. The entire workflow was carried out using **Google Colab** in an integrated manner, assisted by an AI assistant throughout the development process.

The project covers a full data science pipeline — from raw data acquisition and preprocessing, to statistical analysis and result interpretation — applied to a real-world environmental challenge with significant implications for urban climate resilience.

---

## 🎯 Objectives

- Analyze the temporal and spatial dynamics of heat waves affecting the Bucharest area
- Apply data processing and statistical methodologies to identify patterns and trends
- Leverage scientific Python libraries to support environmental and geographical analysis
- Document findings in a clear and reproducible format

---

## 🗂️ Repository Contents

| File | Description |
|------|-------------|
| `README.md` | The context for this project and details about the analysis |
| `notebook.ipynb` | Main Google Colab notebook containing all code, analyses, and visualizations |
| `report.pdf / report.docx` | Detailed document outlining the key findings from the analyses |
| `data.md` | Raw datasets used in the project |
| `heatwave_analysis_prompt.md` | The prompt used for the AI agent |
| `HW_dashboard_interactive.html` | Interactive Plotly dashboard with all heatwave indices |

---

## 🛠️ Methods & Tools

### Platform
- **Google Colab** — cloud-based Jupyter notebook environment
- **Claude Code** — AI assistant for coding and analytical support

### Libraries & Frameworks
The project makes use of widely adopted libraries across data science, environmental sciences, and geography, including but not limited to:

- `pandas`, `numpy` — data manipulation and numerical processing
- `matplotlib`, `seaborn` — data visualization
- `scipy`, `statsmodels` — statistical analysis
- `xarray`, `netCDF4` — handling climate/meteorological datasets
- `geopandas`, `shapely` — geospatial data processing

### Methodology
- Heatwave event detection and heatwave indices (HWN, HWF, HWD, HWM, HWA) following the [climpact methodology](https://climpact-sci.org/indices/)
- Time series analysis of temperature records
- Detection and classification of heat wave events
- Statistical characterization (frequency, intensity, duration)
- Spatial analysis of heat wave distribution across the Bucharest region

---

## 📊 Key Findings

The dashboard below summarizes the evolution of five heatwave indices computed for the **Bucharest Area of Interest (1961–2025)**, based on the **Tx90** threshold (90th percentile of maximum temperature). All indices show a statistically significant **upward trend** over the 64-year period, confirmed by Sen's Slope estimates.

![Heatwave Indices Dashboard — Bucharest AOI (1961–2025)](assets/dashboard_preview.png)

| Index | Description |
|-------|-------------|
| **HWN** | Heatwave Number — count of distinct heatwave events per year |
| **HWF** | Heatwave Frequency — fraction of the year spent in heatwave conditions |
| **HWD** | Heatwave Duration — length of the longest heatwave event |
| **HWM** | Heatwave Magnitude — mean temperature anomaly during heatwaves |
| **HWA** | Heatwave Amplitude — peak temperature anomaly during the hottest event |

> 💡 An interactive version of this dashboard (built with Plotly) is available in [`HW_dashboard_interactive.html`](HW_dashboard_interactive.html) — download and open locally in your browser.

### 🔑 Main Conclusions

- **All five heatwave indices are rising.** HWN, HWF, HWD, HWM and HWA all show statistically significant upward trends over 1961–2025, meaning heatwaves are becoming more frequent, longer, and more intense.

- **The signal is region-wide.** Trend patterns are spatially coherent across the entire Bucharest AOI, pointing to large-scale regional climate forcing rather than localised effects.

- **A clear regime shift after 2000.** Before 1990, heatwaves were irregular and relatively rare. Since 2000, they have become near-annual, multi-event occurrences affecting the whole area simultaneously.

- **2007 as the benchmark extreme.** The 2007 warm season had 30–38% of its days classified as heatwave days across the entire AOI — a striking illustration of the new climate normal.

- **Extreme temperatures are projected to intensify.** Extreme Value Analysis (GEV) estimates a 10-year return temperature of **41.2°C** and a 50-year return of **42.7°C** — and these are likely conservative given ongoing non-stationarity.

- **Compound heat events are accelerating.** Since 2000, the time between successive heatwave events has converged to roughly one year, and intensity anomalies continue to trend upward.

- **Urgent implications for Bucharest.** The findings call for immediate action on heat adaptation planning, revision of infrastructure standards, and prioritisation of urban cooling interventions.

A full technical breakdown can be found in the accompanying report and notebook.

---

## 🚀 Getting Started

To explore the project:

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   ```
2. Open the notebook in [Google Colab](https://colab.research.google.com/) or a local Jupyter environment.

3. Run the cells sequentially to reproduce the analysis.

4. For the interactive dashboard, open `HW_dashboard_interactive.html` directly in your browser.

---

## 👤 Author

**Alexandru Ovedenie** *(Ove)*  
Participant — DeltaHUB Workshop

---

## 📄 License

This project is intended for educational and research purposes. Please reach out before using or redistributing any part of this work.
