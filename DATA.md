# Date Brute — Acces și Replicare

Acest fișier documentează sursa datelor meteorologice utilizate în analiză și oferă instrucțiunile necesare pentru accesarea și replicarea rezultatelor.

---

## Sursa datelor

Fișierele `.nc` (NetCDF) utilizate în această analiză provin din setul de date deschise al Guvernului României:

**Date meteorologice zilnice grilate**
🔗 [https://data.gov.ro/dataset/date-meteorologice-zilnice-gridate](https://data.gov.ro/dataset/date-meteorologice-zilnice-gridate)

Datele sunt disponibile public prin portalul [data.gov.ro](https://data.gov.ro) și pot fi descărcate direct de la link-ul de mai sus.

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

## Replicarea analizei

Pentru a replica analiza, urmează pașii de mai jos:

1. **Descarcă datele brute** de la link-ul de mai sus.
2. **Plasează fișierele `.nc`** în directorul corespunzător din repo (ex: `data/raw/`).
3. **Rulează script-urile de analiză** în ordinea indicată în documentație / notebook-uri.

> **Notă:** Asigură-te că ai instalate librăriile necesare pentru citirea fișierelor NetCDF (ex: `xarray`, `netCDF4`, `cfgrib` pentru Python).

---

## Citare

Dacă folosești aceste date în lucrările tale, te rugăm să citezi sursa originală conform termenilor indicați pe [data.gov.ro](https://data.gov.ro/dataset/date-meteorologice-zilnice-gridate).
