---
layout: default
title: "Buildings and structures"
permalink: /en/content/construcciones/
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

# Buildings of interest — Layer factsheet

**Download:** *[Zenodo](https://doi.org/10.5281/zenodo.18109683)*.   
**Version:** v1.0.0 · **Last updated:** 10-01-2026  
**Licence:** CC BY-NC 4.0  

<figure style="margin: 0 0 1rem 0;">
  <img src="{{ "/assets/img/casalosguardas_red.jpeg" | relative_url }}" alt="Topo Doñana" style="max-width: 100%; height: auto;">
  <figcaption style="font-size: 0.78em; opacity: 0.85; margin-top: 0.35rem; text-align: justify; text-justify: inter-word;">
Casa de los Guardas. Photograph: Miguel de Felipe. 
  </figcaption>
</figure>

---

## 1. Summary

This layer maps **buildings and built features of interest** in Doñana National Park and adjacent areas, for **cartographic, orientative, and outreach** purposes. It includes—though not necessarily exhaustively—**palaces**, **warden houses**, **watchtowers**, **police/border guard barracks**, **lighthouses**, and **visitor centres**.

**Data authorship:** this cartography was **created by the map author** through **photo-interpretation** and local territorial knowledge (cartographic memory and local references), with the aim of integrating, within a single composition, the elements that structure the human reading of the landscape.

**Why it is included in this repository:** to provide a simple GIS layer that enables the **location** of these buildings on the map, their linkage to other thematic layers, and a basis for **future corrections and improvements** by people with knowledge of the territory.

> **Notice:** orientative layer. It is not an official inventory and should not be used for administrative, legal, or cadastral purposes.  
> **Note:** buildings/features that no longer exist are represented in the toponymy layer under the category “disappeared places”.

---

## 2. Content

The dataset is distributed as **two layers**:

### 2.1. Watchtowers and lighthouses
- **File name:** `Watchtowers-Torres_25829.shp`  
- **Feature type:** **Point** shapefile  
- **Mapped feature:** point locations of watchtowers and lighthouses.

### 2.2. Buildings of interest
- **File name:** `Buildings-Costrucciones_25829.shp`
- **Feature type:** **Polygon** shapefile  
- **Mapped feature:** approximate building footprints (palaces, warden houses, barracks, visitor centres, etc.).

---

## 3. Spatial and temporal scope

- **Spatial coverage:** Doñana National Park and nearby elements when relevant to the overall cartographic composition.  
- **Temporal coverage (reference):** digitisation based on photo-interpretation and territorial knowledge available up to **2025**.  
- **Notice:** the presence, condition, or use of some buildings may change over time (demolition, ruin, restoration, repurposing).

---

## 4. Reference system (CRS)

- **CRS / EPSG (layers in this repository):** EPSG:25829 — ETRS89 / UTM zone 29N  
- **Units:** metres (UTM)

---

## 5. Data sources

**Working basis:**  
- Author-led photo-interpretation (high-resolution orthophotography) and territorial knowledge.

**Note:** this layer is not built from a single institutional inventory. It is published as an **original cartographic product**, open to improvement through comparison with official inventories, historical bibliography, or field verification.

---

## 6. Workflow (methods)

- **Step 1. Feature identification**  
  Initial compilation of relevant places and built features (palaces, warden houses, watchtowers, barracks, lighthouses, visitor centres) based on territorial knowledge.

- **Step 2. Digitisation by photo-interpretation**  
  - **Watchtowers and lighthouses:** digitised as **points** placed on the identifiable feature.  
  - **Buildings:** digitised as **polygons** following the visible (approximate) footprint on orthophotos.

- **Step 3. Attribute standardisation and export**  
  Unique IDs were assigned, fields were harmonised, and outputs exported in CRS EPSG:25829.

**Key criteria (definitions):**  
- **Inclusion/exclusion:** clearly identifiable buildings of cultural/functional relevance for a synthesis map are included; minor constructions that are not distinguishable or not relevant to the synthesis are excluded.  
- **Assumptions:** orthophotos allow an approximate delineation adequate for synthesis cartography, but do not guarantee inventory-level precision.

---

## 7. Data structure and attributes

### 7.1. Point layer: watchtowers and lighthouses

| Field | Type | Description |
|---|---|---|
| `id` | integer / string | Unique internal identifier |
| `name` | string | Feature name (tower/lighthouse) |
| `coordx` | double | X coordinate (layer CRS) |
| `coordy` | double | Y coordinate (layer CRS) |

**Missing / null values:** `NULL`

### 7.2. Polygon layer: buildings of interest

| Field | Type | Description |
|---|---|---|
| `id` | integer / string | Unique internal identifier |
| `name` | string | Building name *(in this version: `NULL`)* |
| `coordx` | double | X coordinate (layer CRS) |
| `coordy` | double | Y coordinate (layer CRS) |

**Missing / null values:** `NULL`

> Note: in this version, the **`name`** field in the polygon layer is published empty (`NULL`). It is prepared to be completed in future versions or via contributions/corrections.

---

## 8. Quality control and validation

- **Controls performed:**  
  - Visual review for duplicates (one record per feature) and spatial coherence.  
  - CRS verification (EPSG:25829) and check that geometries fall within the expected area.  
  - Basic manual geometry review (closed polygons; no obvious errors).

- **Validation:**  
  This version relies primarily on photo-interpretation and territorial knowledge. A more exhaustive validation would require comparison with official inventories, historical bibliography, or field verification.

- **Positional accuracy:**  
  Orientative. For uses sensitive to exact positions or building boundaries, specific verification is recommended.

---

## 9. Limitations and appropriate use

- **Recommended uses:**  
  - Synthesis cartography and outreach (location of relevant built features).  
  - Historical and cultural contextualisation within the map.  
  - Orientative support for fieldwork and visit/sampling planning (at park scale).

- **Not recommended for:**  
  - Legal/cadastral delineations, construction planning, permitting, or administrative decisions.  
  - Detailed interpretations (exact dimensions, precise boundaries, conservation status) without verification.

**Specific limitations:**  
- **Not exhaustive**, and **temporal change** is expected (buildings demolished, transformed, repurposed).  
- Possible **identification errors** for features that are hard to distinguish or partially obscured.  
- In the polygon layer, the `name` field remains to be completed in future versions.

---

## 10. Citation

**Recommended citation:**  
M. de Felipe (2026). *Updated Map of Doñana National Park* (v1.0). Zenodo. DOI: https://doi.org/10.5281/zenodo.18109683

---

## 11. Change log (in this repository)

- **v1.0.0 (10-01-2026)** — Creation of the *buildings of interest* layer (polygons) and *watchtowers & lighthouses* layer (points) via photo-interpretation and manual digitisation.

---

## 12. Contact

For questions, corrections, or suggestions (e.g., missing names, buildings not included, changes in status): contact me **[here](mailto:m.defelipe.t@gmail.com)**.
