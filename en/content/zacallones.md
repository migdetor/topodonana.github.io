---
layout: default
title: "Zacallones"
permalink: /en/content/zacallones/
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

# Zacallones, wells and spring eyes — Layer factsheet

**Download:** *[Zenodo](https://doi.org/10.5281/zenodo.18109683)*.

**Version:** v1.0.0 · **Last updated:** 10-01-2026  
**License:** CC BY-NC 4.0  

<figure style="margin: 0 0 1rem 0;">
  <img src="{{ "/assets/img/porquera_red.jpeg" | relative_url }}" alt="Topo Doñana" style="max-width: 100%; height: auto;">
  <figcaption style="font-size: 0.78em; opacity: 0.85; margin-top: 0.35rem; text-align: justify; text-justify: inter-word;">
Monitoring of threatened aquatic plants at *Porquera del Jabato* (La Algaida). Photograph: Miguel de Felipe.
  </figcaption>
</figure>

---

## 1. Summary

This layer maps the location of **zacallones**, **wells**, **troughs/abrevaderos**, and **spring eyes** (*ojos*) in Doñana National Park, as point features, for **cartographic and orientative purposes** and to support territorial interpretation.

In Doñana, **zacallón** is a popular variant of the word *azacaya* (with apheresis and the augmentative suffix *-ón*). *Azacaya* is a word of Arabic origin associated with *water conduits or branches* and, in Doñana, it is used both toponymically and generically to refer to **water coming from an *ojo* (water spring), where livestock drink**. *(DRAE, s.v.; Castrillo Díaz 1994).*  

**Ojos** are **freshwater upwellings** linked to the confined aquifer beneath the clayey substrate of the marsh. They have high ecological value because they constitute one of the **few sources of freshwater during summer**, especially in dry years.

**Data authorship:** this layer is based on a previous dataset from the **monitoring team** of **ICTS Doñana**, which has been **reviewed, expanded, and updated by the author** to reflect the current state of the Park. During this process, elements that had disappeared were removed, locations were corrected, and new points not present in the original dataset were added.

**Reason for inclusion in this repository:** to provide a single, updated GIS layer that integrates these hydraulic and toponymic elements coherently with the map, enabling joint visualization and traceability across future versions.

> **Notice:** indicative layer. This is not an official inventory of hydraulic infrastructure and should not be used for administrative, legal, or operational management purposes without specific verification.

---

## 2. Content

- **Filename:** `zacallones_pozos_ojos_25829.shp` *(adjust to the real name)*  
- **Feature type:** Point shapefile  
- **What is mapped:** locations of zacallones, wells, troughs/abrevaderos, and spring eyes in Doñana.

---

## 3. Spatial and temporal extent

- **Spatial coverage:** Doñana National Park and the restored marsh area (*marisma gallega*) within Doñana Natural Park.
- **Temporal scope (reference):** update based on review and photo-interpretation carried out up to **2025**.
- **Notice:** some elements may have changed over time (siltation, abandonment, destruction, restoration), especially smaller infrastructures.

---

## 4. Coordinate reference system (CRS)

- **CRS / EPSG (layer in this repository):** EPSG:25829 — ETRS89 / UTM zone 29N  
- **Units:** meters (UTM)

---

## 5. Data sources

**Baseline dataset:**  
- Previous dataset from the monitoring team of **ICTS Doñana**.

**Subsequent processing:**  
- The dataset was **modified, reviewed, expanded, and updated by the author** (Section 6), through photo-interpretation and consultations.

---

## 6. Workflow (methods)

- **Step 1. Review and cleaning of the baseline dataset (ICTS Doñana)**  
  Spatial coherence and duplicate records were checked. Points with uncertainty or potential obsolescence were flagged (absent or transformed elements).

- **Step 2. Verification by photo-interpretation**  
  Using high-resolution orthophotos, the presence/absence of features (especially wells, troughs/abrevaderos, and associated structures) was assessed. Locations were corrected when needed and points without current evidence were removed.

- **Step 3. Expansion and updating through local and expert consultation**  
  New points not included in the baseline were added based on **consultations with experts and local knowledge holders**, prioritizing toponymic coherence and traditional use knowledge.

- **Step 4. Standardization and export**  
  Fields, coding, and formats were harmonized. The final product was exported as a shapefile in EPSG:25829.

**Key criteria (definitions):**  
- **Inclusion/exclusion:** features are included when identifiable (orthophoto evidence and/or confirmation through local/expert knowledge). Points are excluded when their current existence cannot be supported by available evidence.  
- **Assumptions:** photo-interpretation provides a reasonable check for synthesis cartography, but it does not replace field verification for small features or those under vegetation cover.

---

## 7. Data structure and attributes

| Field | Type | Description |
|---|---|---|
| `id` | integer / string | Unique internal identifier |
| `tipo` | string | Feature type (`zacallon`, `pozo`, `abrevadero`, `ojo`) |
| `status` | string | Condition/status (`degraded`, `good`, `NULL`) |
| `nombre` | string | Name / toponym (if available) |
| `coordx` | double | X coordinate (layer CRS) |
| `coordy` | double | Y coordinate (layer CRS) |

**Missing / null values:** `NULL`

---

## 8. Quality control and validation

- **Checks performed:**  
  - Duplicate screening and spatial consistency (CRS EPSG:25829).  
  - Visual inspection by photo-interpretation for critical or uncertain points.  
  - Harmonization of typologies and attribute coding.

- **Validation:**  
  - Cross-checking between the baseline dataset (ICTS Doñana), photo-interpretation, and expert/local consultations.  
  - Full validation would require systematic field verification.

- **Known issues:**  
  - **Limited detectability** due to vegetation cover, shadow, or small feature size.  
  - **Temporal uncertainty:** some points can change quickly (siltation, restoration, abandonment).  
  - **Toponymic variability:** the same feature may have local name variants.

- **Positional accuracy:**  
  Indicative. For uses sensitive to exact position, field verification or cross-checking with official sources is recommended.

---

## 9. Limitations and appropriate use

- **Recommended uses:**  
  - Synthesis cartography and ecological/cultural contextualization of the territory.  
  - Orientative support for surveys and field work (park-scale).  
  - Exploratory spatial analysis at scales compatible with the product’s effective resolution.

- **Not recommended for:**  
  - Administrative/legal decisions or operational inventories without field verification.  
  - Uses requiring exact location or current functional characterization (status, flow, accessibility).

**Specific limitations:**  
- Photo-interpretation and consultations improve the baseline, but do not guarantee exhaustiveness or temporal permanence. This layer should be understood as an **indicative and updateable** representation.

---

## 10. Citation

**Recommended citation:**  
M. de Felipe (2026). *Updated map of Doñana National Park* (v1.0). Zenodo. DOI: https://doi.org/10.5281/zenodo.18109683

---

## 11. Change history (in this repository)

- **v1.0.0 (10-01-2026)** — Review, expansion, and update of the zacallones/wells/troughs/spring eyes dataset (derived from a previous ICTS Doñana dataset), using photo-interpretation and consultations.

---

## 12. Contact

For questions, corrections, or contributions (e.g., current existence, local naming, new locations): contact me **[here](mailto:m.defelipe.t@gmail.com)**.
