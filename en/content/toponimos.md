---
layout: default
title: "Toponyms"
permalink: /en/content/toponimos/
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

# Toponyms — Layer factsheet

**Download:** [Zenodo](https://doi.org/10.5281/zenodo.18109683).

**Version:** v1.0.0 · **Last updated:** 10-01-2026  
**License:** CC BY-NC 4.0  

<figure style="margin: 0 0 1rem 0;">
  <img src="{{ "/assets/img/mapmarsh_red.jpg" | relative_url }}" alt="Topo Doñana" style="max-width: 100%; height: auto;">
  <figcaption style="font-size: 0.78em; opacity: 0.85; margin-top: 0.35rem; text-align: justify; text-justify: inter-word;">
Fragment of the updated map of Doñana National Park. 
  </figcaption>
</figure>

---

## 1. Summary

This layer compiles **historical and current toponymy** for Doñana National Park and its immediate surroundings, for **cartographic, cultural, and socio-ecological interpretation** purposes.

The core of the layer is based on the **place names used by J. Castroviejo (1993)** in the *Map of Doñana National Park*, which were **manually extracted** and then **checked, corrected, expanded, and hierarchized**. The aim is to preserve coherence with the foundational toponymy of that reference map, while giving it an operational structure that distinguishes place type, scale, and permanence in the landscape.

**Data authorship:** this layer has been **compiled and edited by the map author** from Castroviejo (1993), personal knowledge of the territory, historical sources (reports, books, earlier cartography), and consultations with local people and experts.

**Living dataset:** the layer is under **continuous revision and improvement**, adding new toponyms and adjusting names, categories, and locations whenever errors are detected or new information becomes available.

---

## 2. Content

The dataset is distributed as **two layers**:

### 2.1. Point toponymy (points)
- **Filename:** `toponimia_25829.shp`
- **Feature type:** Point shapefile  
- **What is mapped:** toponyms that can be represented as a cartographic point (including “zone” or “estate” names represented by a reference point).

### 2.2. Linear toponymy (lines)
- **Filename:** `toponimia_lineal_25829.shp`  
- **Feature type:** Line shapefile  
- **What is mapped:** linear features (mainly **streams**, **channels**, and other linear hydrological elements) whose names are not adequately represented as a point.

---

## 3. Spatial and temporal extent

- **Spatial coverage:** Doñana National Park and adjacent areas included in the map (as defined by the project’s cartographic composition).  
- **Temporal scope (reference):** integrates historical toponymy (Castroviejo 1993) and current usage (based on recent sources and local knowledge).  
> **Notice:** toponymy may change due to local usage, phonetic variation, administrative officialization, or landscape transformation (loss of ponds, land-use change, disappearance of buildings).

---

## 4. Coordinate reference system (CRS)

- **CRS / EPSG (layers in this repository):** EPSG:25829 — ETRS89 / UTM zone 29N  
- **Units:** meters (UTM)

---

## 5. Data sources

**Starting point (reference toponymy):**  
- Castroviejo, J. (1993). *Mapa del Parque Nacional de Doñana* *(adjust full citation to your bibliography)*.

**Subsequent processing:**  
- The reference set was **manually extracted** and later **corrected, expanded, and hierarchized by the author** (Section 6).

**Additional sources:**  
- Historical sources (books, reports, earlier cartography).  
- Consultations with local and expert informants.  
- Personal knowledge of the territory.

> Note: given the cultural and partly oral nature of toponymy, some entries may present variants in spelling, pronunciation, or local usage.

---

## 6. Workflow (methods)

- **Step 1. Manual extraction of the toponymic baseline (Castroviejo 1993)**  
  Place names were transcribed from the original map and assigned a location for cartographic representation once their meaning and context were checked.

- **Step 2. Review, correction, and standardization**  
  Spelling, duplicates, and internal consistency (repeated terms, variants) were reviewed, standardizing formats and fields.

- **Step 3. Expansion and cross-checking of sources**  
  Additional toponyms were incorporated from historical sources, bibliography, and local/expert consultations, maintaining conceptual traceability with the reference map.

- **Step 4. Hierarchization and thematic classification**  
  Operational categories were defined to distinguish scale and nature of the place name (see Section 7), including the hydrological distinction between **sands** and **marsh**.

- **Step 5. Geometric representation (points and lines)**  
  - **Points** were used for non-linear toponyms (including zones/estates represented by a reference point).  
  - **Lines** were used for clearly linear elements (streams, channels, and similar).

---

## 7. Data structure and attributes

### 7.1. Attributes (point layer)

| Field | Type | Description |
|---|---|---|
| `fid` | (OID) / integer | Internal identifier |
| `categoria` | string | Hierarchical category of the toponym *(see below)* |
| `nombre` | string | Name / toponym |
| `tipo` | string | Thematic type (e.g., hydrology/sands/marsh, building, estate, etc.) |
| `coordx` | double | X coordinate (layer CRS) |
| `coordy` | double | Y coordinate (layer CRS) |

**Categories used (`categoria`)** *(as currently defined in your project):*  
- `hito` (specific landmarks/points; e.g., *Alcornoque Escobar*, *Alameda de Alcuña*)  
- `zona` (spatial unit; e.g., *Corral Mahón*)  
- `finca` (large traditional spatial unit; e.g., *Marismillas*)  
- `edificacion` (built features; e.g., *Palacio de Doñana*)  
- `desaparecido` (disappeared places; e.g., *Laguna del Brezo*, *Casa de Marilópez*)  
- `hidrologia` (hydrological toponyms; see `tipo` for sands/marsh subtyping)

**Missing / null values:** `NULL`

**Key definitions:**  
- **Zones and estates:** although represented with point coordinates, they should be understood as **spatially extensive units**; the point is a cartographic reference, not an exact location.  
- **Disappeared places:** toponyms associated with features that no longer exist due to ecological or human-driven change (e.g., pond desiccation, demolition of buildings).  
- **Hydrology:** distinction is made between names linked to **sandy systems** (ponds, streams, sandy channels) and names specific to the **marsh** (channels, *lucios*, etc., where applicable).

### 7.2. Attributes (line layer)

| Field | Type | Description |
|---|---|---|
| `fid` | (OID) / integer | Internal identifier |
| `categoria` | string | Hierarchical category *(e.g., `hidrologia`)* |
| `nombre` | string | Name / toponym |
| `tipo` | string | Thematic type (e.g., `arroyo`, `caño`, `marisma`, `arenas`) |

---

## 8. Quality control and validation

- **Checks performed:**  
  - Review of duplicates and spelling standardization (local variants, diacritics, capitalization).  
  - Categorical consistency (same logic for `categoria` and `tipo`).  
  - Basic spatial checking (toponyms within map extent and coherent with landscape units).

- **Validation:**  
  - Cross-checking against the reference map (Castroviejo 1993).  
  - Verification via local knowledge and consultations with local/expert informants when possible.

- **Limitations:**  
  - **Spatial uncertainty:** for `zona` and `finca`, the point is representative and does not delineate the real area.  
  - **Linguistic variability:** the same place may appear with spelling or pronunciation variants.  
  - **Temporal change:** some names fall out of use; others become official or shift over time.

- **Positional accuracy:**  
  Indicative. This is not a legal boundary or official gazetteer product; for sensitive uses, contrast with official sources or verify in situ.

---

## 9. Limitations and appropriate use

- **Recommended uses:**  
  - Map synthesis and outreach (cultural reading of the landscape).  
  - Support for research or territorial interpretation requiring a coherent, traceable toponymic base.  
  - Orientation and contextualization of ecological and historical layers within the map.

- **Not recommended for:**  
  - Administrative/legal uses or decisions requiring an official gazetteer.  
  - Inferring real spatial boundaries from points.  
  - Fine-scale navigation or location without specific verification.

---

## 10. Citation

**Recommended citation:**  
M. de Felipe (2026). *Updated map of Doñana National Park* (v1.0). Zenodo. DOI: https://doi.org/10.5281/zenodo.18109683

---

## 11. Change history (in this repository)

- **v1.0.0 (10-01-2026)** — Manual extraction of toponyms from Castroviejo (1993) and expanded compilation (correction, expansion, hierarchization, and classification; inclusion of a line layer for streams and channels).

---

## 12. Contact

For corrections, local variants, missing toponyms, or discussion of categories: contact me **[here](mailto:m.defelipe.t@gmail.com)**.
