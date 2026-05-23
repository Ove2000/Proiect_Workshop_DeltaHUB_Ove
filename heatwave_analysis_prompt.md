# Heatwave Dynamics Analysis — Initial Prompt

> This document captures the original prompt used to initiate a heatwave dynamics analysis for the Bucharest, Romania area using Google Colab, NetCDF datasets, and climatological indices. It is preserved here for reproducibility and transparency.

---

## Prompt

I want you to write the code for me in Google Colab. I want to achieve an analysis of the dynamics of heatwaves in the area of Bucharest, Romania.

1. I want you to perform all the analysis in this folder on my Google Drive: `My Drive > Workshop_DeltaHUB > 00_Proiectul_meu`.

2. I have a NetCDF dataset (`.nc`) for maximum daily temperature from ANM. It is stored in my Google Drive. The path to the data is: `My Drive > ANM_Datasets > 01_Temperatura_maxima`. I want you to take this data and import the NetCDF datasets.

3. I also have an Area of Interest (AOI) stored in Google Drive: `My Drive > Workshop_DeltaHUB > 00_Proiectul_meu > 00_Baza_date > 01_AOI`. It is an archived Shapefile (`.shp`). I want you to unarchive this AOI and use it for the analysis.

4. First of all, I want you to inspect the data and extract only the pixels that fall within the Area of Interest (AOI). I want only the values that are reliable and representative of reality. Mask the `.nc` files only for this area.

5. I also think that you need to regrid the data for the most recent years — 2023, 2024, and 2025 — if I am not mistaken. Please verify this for me.

6. I want you to merge them into a single NetCDF file containing all daily maximum temperatures for all years (1961–2025).

7. I want you to convert the file format from `.nc` to `.zarr` for enhanced usability.

8. I want you to use the methodology for heatwave calculation based on the information from [https://climpact-sci.org/indices/](https://climpact-sci.org/indices/).

9. Based on this methodology, I want to obtain the following indices: `Tx90-HWN`, `Tx90-HWF`, `Tx90-HWD`, `Tx90-HWM`, `Tx90-HWA`.

10. I want you to use **1971–2000** as the baseline period. I also want you to set the minimum number of consecutive days that define a heatwave event to **3 consecutive days** where TX exceeds the 90th percentile of the baseline period. This is the definition from the site:

    > *"Heatwave number (HWN) as defined by the 90th percentile of TX: the number of individual heatwaves that occur each summer (Nov–Mar in the southern hemisphere and May–Sep in the northern hemisphere). A heatwave is defined as 3 or more days where TX > 90th percentile, where percentiles are calculated from the base period specified by the user."*

11. I want those indices to be calculated across the AOI and to produce a file that shows, for example, heatwave events day by day and how they evolve across time and space.

12. After that, I want you to apply the **Seasonal Mann-Kendall trend test** to all 5 heatwave indices in order to extract the trend and significance, tau value, slope, and intercept.

13. I also want you to apply a **seasonal decomposition** function to all 5 heatwave indices to identify whether variability originates from natural variability, seasonality, or trend.

14. I want you to generate maps for each heatwave index and make them interactive, with pop-ups available for each pixel. I want to be able to click on each pixel and identify the stored values, the trends and Sen's slope from the Mann-Kendall trend test, and the seasonal decomposition results.

15. I also want you to create `.zarr` files for each heatwave index, to be usable in GIS programs. I want the same for the seasonal decomposition and for the Mann-Kendall trend test results.

16. Please suggest what other types of additional analyses and plots could be relevant for this type of data.

17. Review the information I have provided and assess the feasibility of implementing this as code. I want you to provide the code **block by block** to make it easier to manage.

18. Write the code for me!

---

*Analysis area: Bucharest, Romania | Data source: ANM (Romanian National Meteorological Administration) | Period: 1961–2025 | Baseline: 1971–2000*
