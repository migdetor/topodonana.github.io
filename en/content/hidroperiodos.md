---
layout: default
title: "Flood duration"
permalink: /en/content/hidroperiodos/
menu:
  - label: "Home"
    url: "/es/"
  - label: "Doñana"
    url: "/en/doniana/"
  - label: "Antecedents"
    url: "/en/preface/"
  - label: "The map"
    url: "/en/map/"
  - label: "Interactive map"
    url: "/interactive/"
  - label: "Cartographic information"
    url: "/en/content/"
  - label: "Data download"
    url: "https://doi.org/10.5281/zenodo.18109683"

links:
  - label: "Contact me"
    url: "/contact/"

citation_label: "Reccomended citation"
citation_text: "M. de Felipe (2026). Mapa actualizado del Parque Nacional de Doñana (v1.0). Zenodo."
citation_doi_label: "DOI: [DOI]"
citation_doi_url: "https://doi.org/10.5281/zenodo.18109683"

---

# Hydroperiods — Layer factsheet

> **Methodological source / protocol:** Laboratory of GIS and Remote Sensing (LAST-EBD, CSIC), following the Landsat-based flooding and hydroperiod reconstruction approach described by [Díaz-Delgado et al. (2016)](https://www.mdpi.com/2072-4292/8/9/775).  
> **Download:** *[Zenodo](https://doi.org/10.5281/zenodo.18109683)*.
 
> **Version:** v1.0.0 · **Last updated:** 10-01-2026  
> **License:** CC BY-NC 4.0

<figure style="margin: 0 0 1rem 0;">
  <img src="{{ "/assets/img/laguna_red.jpeg" | relative_url }}" alt="Topo Doñana" style="max-width: 100%; height: auto;">
  <figcaption style="font-size: 0.78em; opacity: 0.85; margin-top: 0.35rem; text-align: justify; text-justify: inter-word;">
Laguna de las Pajas. In the background, the Grazalema range. Photograph: Miguel de Felipe. 
  </figcaption>
</figure>

---

## 1. Summary

These layers represent **hydroperiod** (annual flood duration) in Doñana derived from Landsat imagery, expressed as categories of **flooded days per year**. Here, hydroperiod is understood as the length of time that a given point in the marsh or a pond remains flooded over an annual cycle (**1 September to 31 August**), derived from binary flood masks applied to a Landsat time series and subsequently aggregated by hydrological year.

This repository distributes two different products, intended to reflect “representative” dynamics for each subsystem:
- **Ponds:** *reference year 2003* (considered “normal” in terms of rainfall for pond dynamics).
- **Marsh:** *reference year 2017* (considered “normal” for marsh dynamics).

The original rasters (hydroperiod for each **30 × 30 m** pixel) were *polygonized* and reclassified into **six** annual inundation-duration classes:  
*0–60 days, 61–120, 121–180, 181–240, 241–300, and 301–365 days*.

**Data authorship:** the cartographic product (class polygons) was prepared by the map’s author from hydroperiod raster products generated following the Landsat protocol used by LAST-EBD (CSIC).

> *Ecological note:* many ephemeral ponds may not flood at all, or only very briefly, in average years; their spatial signal may become clearly detectable only in wet years. Therefore, these layers should be interpreted as a representative snapshot of hydroperiod for the selected years, not as an exhaustive inventory of all floodable ponds. For the latter, consult the [ponds cartography]({{ "/en/content/lagunas/" | relative_url }}).

---

## 2. Content

This dataset includes two vector layers (polygons) derived from hydroperiod rasters:

### 2.1. Hydroperiod — Ponds (reference year 2003)
- **Filename:** `hidroperiodo_lagunas_2003_25829.shp`
- **Feature type:** Polygon shapefile
- **What is mapped:** annual inundation-duration classes associated with ponds (sands) for year 2003.

### 2.2. Hydroperiod — Marsh (reference year 2017)
- **Filename:** `hidroperiodo_marisma_2017_25829.shp` *(adjust to the actual name)*
- **Feature type:** Polygon shapefile
- **What is mapped:** annual inundation-duration classes in the marsh for year 2017.

---

## 3. Spatial and temporal extent

- **Spatial coverage:** Doñana National Park and areas mapped in the project (according to the applied clipping extent).
- **Temporal coverage:**  
  - *Ponds:* **2003** (reference year).  
  - *Marsh:* **2017** (reference year).
- **Hydroperiod temporal definition:** annual duration in days per cycle (**1 September** to **31 August**), based on aggregation of inundation masks derived from Landsat time series.

---

## 4. Coordinate reference system (CRS)

- **CRS / EPSG:** EPSG:25829 — ETRS89 / UTM zone 29N
- **Units:** meters (UTM)

---

## 7. Data structure and attributes

### Fields used in this project

| Field | Type | Description |
|---|---|---|
| `fid` | integer | Internal identifier |
| `class` | string / integer | Hydroperiod class (integer 1–6) |
| `dias_min` | integer | Lower bound of the range |
| `dias_max` | integer | Upper bound of the range |
| `anio_ref` | integer | Reference year (2003 or 2017) |
| `area` | integer | Area covered by each hydroperiod class (hectares) |

---

## 9. Limitations and appropriate use

**Recommended uses:**
- Synthesis mapping of the flooding gradient (hydroperiod) in ponds and marsh.
- Ecological context (habitats associated with different water permanency).
- Exploratory and comparative analyses (e.g., overlay with vegetation, toponyms, infrastructure, etc.) at a scale compatible with the data resolution.

**Not recommended for:**
- Legal/juridical delineations or operational decisions requiring fine metric precision.
- Inferring water presence/absence in years other than the reference year without accounting for climatic and hydrological variability.
- Diagnosing very small ponds or narrow linear features (minor channels/streams) below the effective resolution.

**Specific limitations:**
- A **single reference year** per subsystem does not capture interannual variability (wet vs. dry years).  
- **Landsat resolution (30 m)** simplifies flood edges and may under-represent small basins.  
- **Ephemeral ponds** may be under-represented in “average” years if they do not flood or do so only briefly.

> **Note (impacts before 2003):** although the selected years are intended to represent a comparatively “normal” functioning of the pond network and the marsh, impacts on the pond network **began before 2003**. Therefore, the hydroperiod layer—while describing a network that may appear in relatively good condition— **could already be partially affected by groundwater abstractions** and earlier hydrological alterations.

---

## 10. Citation

**Recommended citation (repository / map):**  
M. de Felipe (2026). *Updated Map of Doñana National Park* (v1.0). Zenodo. DOI: https://doi.org/10.5281/zenodo.18109683

**Method citation (Landsat-hydroperiod protocol):**  
Díaz-Delgado, R., Aragonés, D., Afán, I., & Bustamante, J. (2016). Long-Term Monitoring of the Flooding Regime and Hydroperiod of Doñana Marshes with Landsat Time Series (1974–2014). *Remote Sensing*, 8, 775. https://doi.org/10.3390/rs8090775

---

## 11. Layer change history (in this repository)

- **v1.0.0 (10-01-2026)** — Release of polygonized hydroperiod-class layers for: (i) ponds (reference year 2003) and (ii) marsh (reference year 2017), derived from rasters.

---

## 12. Contact

For questions, corrections, or suggestions, contact me [here](mailto:m.defelipe.t@gmail.com).
