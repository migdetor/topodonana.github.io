---
layout: default
title: "Hydromet Stations"
permalink: /en/content/hidromet/
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

# Hydrometeorological stations (ICTS-RBD) — Layer factsheet

>**Source (data access):** [HIDROMET (ICTS-RBD)](https://datos-automaticos.icts.ebd.csic.es/es/)  
>**Technical documentation (PDF):** see [HIDROMET documentation](https://datos-automaticos.icts.ebd.csic.es/es/info/).

>**Download:** *[Zenodo](https://doi.org/10.5281/zenodo.18109683)*.

>**Version:** v1.0.0 · **Last updated:** 10-01-2026  
>**Licence:** CC BY-NC 4.0

<figure style="margin: 0 0 1rem 0;">
  <img src="{{ "/assets/img/cancelamillan_red.jpeg" | relative_url }}" alt="Topo Doñana" style="max-width: 100%; height: auto;">
  <figcaption style="font-size: 0.78em; opacity: 0.85; margin-top: 0.35rem; text-align: justify; text-justify: inter-word;">
Hydrometeorological station “Cancela Millán”, in the *castañuela* marsh. Photograph: Miguel de Felipe. 
  </figcaption>
</figure>

---

## 1. Summary

This layer contains the **locations of hydrometeorological stations** integrated in **HIDROMET**, the database of the **[ICTS–Doñana Biological Reserve (ICTS-RBD)](https://icts-donana.csic.es)** that stores hydrometeorological time series recorded by automatic stations distributed across Doñana.

HIDROMET stations record high-frequency environmental data (e.g., every 5 minutes) as well as aggregated products (hourly, daily, monthly). For details on the variables measured at each station, temporal resolution, aggregation, quality control, and updates, consult **[the platform and its technical documentation](https://datos-automaticos.icts.ebd.csic.es/es/)**.

**Data authorship:** this layer **is not intended as an official HIDROMET product**. It is a **cartographic derivative** prepared by the map author to facilitate visualization and integration within the project.

**Why it is included in this repository:** to provide a single GIS layer (point shapefile) for **map display** and as a direct **link to the official data portal**. For data access and operational metadata, consult:  
[https://datos-automaticos.icts.ebd.csic.es/es/](https://datos-automaticos.icts.ebd.csic.es/es/)

---

## 2. Content

- **File name:** `hidromet_25829.shp`  
- **Feature type:** Point shapefile  
- **Mapped feature:** HIDROMET station locations in Doñana (station points)

---

## 3. Spatial and temporal scope

- **Spatial coverage:** Doñana National Park / the set of stations managed in HIDROMET (ICTS-RBD)  
> **Notice:** this layer represents **station points**; it does not replace the official platform and does not imply completeness beyond the stations integrated in HIDROMET.

---

## 4. Reference system (CRS)

- **CRS / EPSG (layer in this repository):** EPSG:25829 — ETRS89 / UTM zone 29N  
- **Units:** metres (UTM)

---

## 5. Data sources

**Primary (official) source:**  
- HIDROMET (ICTS-RBD): https://datos-automaticos.icts.ebd.csic.es/es/

**Redistribution note:** this website/repository provides a *convenience layer* to integrate stations into the map; the official reference for data products, variables, and conditions of use should be taken from HIDROMET.

---

## 6. Workflow (methods)

*Not applicable.*

---

## 7. Data structure and attributes

**Stations included (according to HIDROMET documentation):**  
Cancela Millán, Hondón del Burro, Lucio del Rey, Resolimán, Vetalengua, Juncabalejo, FAO, and Brenes.

**Layer attributes (cartographic derivative):** *(adjust field names if your shapefile differs)*

| Field | Type | Description |
|---|---|---|
| `id` | integer / string | Unique internal identifier |
| `nombre` | string | Station name (e.g., *Lucio del Rey*) |
| `coordx` | double | X coordinate (layer CRS) |
| `coordy` | double | Y coordinate (layer CRS) |

**Missing / null values:** `NULL`

---

## 8. Quality control and validation

See the associated documentation in **[HIDROMET (ICTS-RBD)](https://datos-automaticos.icts.ebd.csic.es/es/)**.

---

## 9. Limitations and appropriate use

- **Recommended uses:**  
  - Synthesis cartography (station locations) and orientation.  
  - Quick access to the official data portal (via HIDROMET links).  
  - Support for fieldwork and sampling planning, respecting the effective scale of the product.

- **Not recommended for:**  
  - Legal/juridical delineations or decisions requiring fine-scale positional accuracy without specific verification.  
  - Interpretations beyond the temporal/methodological scope described in the official platform.

---

## 10. Citation

**Recommended citation (cartographic layer in this repository):**  
M. de Felipe (2026). *Updated Map of Doñana National Park* (v1.0). Zenodo. DOI: https://doi.org/10.5281/zenodo.18109683

**Recommended citation (official data source):**  
HIDROMET (ICTS-RBD): https://datos-automaticos.icts.ebd.csic.es/es/

---

## 11. Change log (in this repository)

- **v1.0.0 (10-01-2026)** — Creation of the HIDROMET station layer (point shapefile) and publication in the repository.

---
