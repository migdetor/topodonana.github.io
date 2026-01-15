---
layout: default
title: "Cork oaks"
permalink: /en/content/alcornoques/
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

# Cork oaks in Doñana National Park — Layer factsheet

> **Download:** *[Zenodo](https://doi.org/10.5281/zenodo.18109683)*.
> 
> **Version:** v1.0.0 · **Last updated:** 10-01-2026  
> **Licence:** CC BY-NC 4.0

<figure style="margin: 0 0 1rem 0;">
  <img src="{{ "/assets/img/308_red.jpeg" | relative_url }}" alt="Topo Doñana" style="max-width: 100%; height: auto;">
  <figcaption style="font-size: 0.78em; opacity: 0.85; margin-top: 0.35rem; text-align: justify; text-justify: inter-word;">
Identification plate of cork oak '308' installed in the 1960s. Photograph: Miguel de Felipe. 
  </figcaption>
</figure>

---

## 1. Summary

Tagging of centuries-old cork oaks was one of the first tasks that J. A. Valverde assigned in 1963 to senior wardens Antonio Chico and José Boixo in the then nascent Doñana Biological Reserve (RBD). The cork oaks were tagged with small wooden plates branded with a unique number; in total, 454 cork oaks were tagged, and 136 of them were photographed in 1966 by [Lorenzo García](https://ealorenzogarcia.wordpress.com/la-figura-de-lorenzo-garcia/), from the Almería Acclimatization Centre (CSIC). During 1989–1990, Juan Carlos Solís produced the first cartography of the cork oaks in the RBD. Based on that cartography, GPS positions were collected in 2008–2012, and 315 individuals were found to be alive ([Ramo & Calderon 2013](http://libros.csic.es/product_info.php?products_id=752)). Building on this dataset—and in response to cork oak dieback linked to heronries and holm oak decline—Dr. Cristina Ramo initiated monitoring of ~250 cork oaks, including 133 individuals systematically monitored in the Doñana Biological Reserve and 119 monitored opportunistically across the National Park. In 2023, poor aquifer status in Doñana was associated with the death of [7% of the cork oaks in the Biological Reserve in less than one year](https://efeverde.com/alcornoques-reserva-biologica-donana/).

To highlight the abundance and distribution of these centuries-old cork oaks, we compiled and combined existing datasets for the RBD cork oak woodland and expanded them through orthophoto interpretation to cover the **entire National Park**. In total, **2,584 cork oaks** that were alive up to 2022 were identified.

**Download the photographic catalogue of the RBD cork oaks** by Ramo & Calderon (2013) [here](http://libros.csic.es/product_info.php?products_id=752)

---

## 2. Content

- **File name:** `alcornoques_25829.shp`
- **Feature type:** Point shapefile
- **Mapped feature:** Individual cork oaks (_Quercus suber_) within Doñana National Park.

---

## 3. Spatial and temporal scope

- **Spatial coverage:** Doñana National Park  
- **Temporal coverage:** June–July 2022 

> **Note:** not suitable for boundary demarcations or legal decisions (if applicable).

---

## 4. Reference system (CRS)

- **CRS / EPSG:** EPSG:25829 — ETRS89 / UTM zone 29N (projected)
- **Units:** individuals (trees) of _Quercus suber_.

---

## 5. Data sources

**Starting point:** compilation of previous sources.  
**Subsequent processing:** the dataset was ***modified, expanded, and harmonised by the author*** (Section 6).

- Solís, J. C. (1996). *Plan de ordenación del alcornocal de Doñana*. Technical report, 105 pp
- Ramo, C. & Calderón, J. (2013). *Mapa y catálogo de los alcornoques centenarios de la Reserva Biológica de Doñana*. 

---

## 6. Workflow (methods)

- **Step 1. Compilation and cleaning of baseline datasets**  
  We started from C. Ramo’s cork oak monitoring dataset (including the individuals inventoried in Ramo & Calderón 2013). Spatial coherence was checked and **only individuals considered alive up to 2022 were retained**, excluding those confirmed dead prior to 2023.  
  The dataset was then **expanded** by incorporating additional individuals reported alive in Solís (1996), harmonising fields and identifiers to avoid duplicates.

- **Step 2. Targeted search for new occurrences via photo-interpretation**  
  Using the cleaned baseline as a guide, a systematic (manual) scan was conducted across the main habitat units where cork oaks are likely to occur (**monte negro**, **vera**, and **pond margins**), identifying tree stands potentially corresponding to _Quercus suber_.

- **Step 3. Height-based filtering using a vegetation surface model**  
  The **Digital Vegetation Surface Model (MDSnV2,5; 2nd coverage; ETRS89 / H29N)** was used to retain only vegetation formations with heights **between 4 and 20 m**, with the goal of:  
  (i) excluding stands typically taller or structurally distinct (e.g., pines, poplars, ashes, tall eucalyptus) and  
  (ii) removing tall shrubland and other non-arboreal covers.

- **Step 4. Final validation using the most recent PNOA orthophoto**  
  Remaining candidates were **individually interpreted** using the most recent PNOA orthophoto for Doñana (**June–July 2022**), confirming diagnostic traits compatible with cork oak and discarding false positives.

- **Step 5. Resolving uncertainties with historical orthophoto series**  
  For doubtful cases, earlier orthophotos were consulted to distinguish young stands (common in recent pine expansion/plantations) from long-persistent individuals or patches consistent with the centuries-old character of Doñana cork oaks.

- **Step 6. Integration, standardisation, and export**  
  Confirmed individuals were merged into a single point layer. Attributes were standardised and the final product exported as a shapefile.

**Key criteria (definitions):**  
- **Inclusion/exclusion:**  
  - *Inclusion:* individuals or tree formations interpreted as _Quercus suber_ within Doñana National Park, confirmed by photo-interpretation (PNOA 2022) and/or present in verified baseline datasets.  
  - *Exclusion:* individuals confirmed dead before 2023 (in the monitoring dataset), and patches discarded due to traits inconsistent with cork oak or corresponding to other species/vegetation structures.

- **Thresholds/codes:**  
  - *Height filter (MDSnV2,5):* **4–20 m** (selection of plausible tree formations; exclusion of tall shrubland and typically taller tree stands).  
  - *Decision rule in doubtful cases:* consultation of historical orthophotos; prioritisation of temporal persistence and diagnostic traits compatible with _Q. suber_.

- **Assumptions:**  
  - The 2022 PNOA orthophoto enables identification of diagnostic traits at an interpretation scale suitable for an orientative (non-legal) inventory.  
  - The 4–20 m filter reduces false positives but can introduce false negatives (e.g., shorter individuals due to stress, regeneration, or local conditions).  
  - Using historical orthophotos improves separation of young pine stands from older, persistent formations, although it is not a direct dating method.

---

## 7. Data structure and attributes

The file includes a field “dictionary”.

| Field | Type | Description | Units / codes |
|---|---|---|---|
| ID | string | Unique identifier for each tree | Sequential number |
| Alcornoque | integer | Individual code from the branded plates | Code |
| diametro | integer | Diameter at breast height (DBH) | Centimetres |
| coordx | integer | X coordinate | EPSG:25829 |
| coordy | integer | Y coordinate | EPSG:25829 |

**Missing / null values:** _NULL_ 

---

## 8. Quality control and validation

- **Controls performed:**  
  - **Duplicate removal:** consolidation of records from Solís (1996) and Ramo & Calderón (2013), checking spatial overlaps.  
  - **Spatial consistency:** verification that all points fall **within Doñana National Park** and in the declared **CRS (EPSG:25829)**.  
  - **Systematic visual review:** manual inspection of each candidate after MDSnV filtering to discard false positives (pine stands, eucalyptus, tall broadleaf stands, tall shrubland).  
  - **Basic QA/QC rules:** checking null values in mandatory fields (e.g., `ID`), harmonising coding and attribute formats.

- **Validation:**  
  - **Direct photo-interpretation** using the most recent PNOA orthophoto (June–July 2022), based on crown/structure traits and context (see Section 6).  
  - **Comparison with previous sources:** cross-check against C. Ramo’s monitoring dataset (including Ramo & Calderón 2013) and Solís (1996) cartography.  
  - **Auxiliary temporal validation:** consultation of historical orthophotos to resolve doubtful cases and discriminate young pine stands from persistent formations compatible with cork oaks.

- **Known issues (limitations):**  
  - **False negatives:** the height filter (4–20 m) may exclude shorter individuals (due to water stress, pruning, open structure) or isolated cork oaks partially obscured by shrub cover.  
  - **Residual false positives:** despite review, some formations may be confused with other broadleaf species or mixed stands in shaded areas, dense mosaics, or under limited resolution.  
  - **Detectability bias:** detection probability is higher in open units (vera, pond margins) than in dense stands or continuously covered areas.  
  - **Temporal uncertainty:** the product represents individuals **alive up to 2022** according to sources and interpretation; it does not reflect subsequent mortality or recent recruitment.

- **Positional accuracy (if known):**    
If the intended analysis is sensitive to exact position (e.g., fine-scale distances), **field verification** or comparison with GPS-based sources is recommended.

---

## 9. Limitations and appropriate use

- **Recommended uses:**  
  - Synthesis cartography and **visualisation** of cork oak (_Quercus suber_) distribution at National Park scale.  
  - Support for **exploratory analyses** (e.g., broad spatial patterns, relationships with environmental units, proximity to ponds), always at a scale compatible with the effective resolution of the product.  
  - **Orientative planning** of sampling and field surveys (area prioritisation, transect design, etc.).  
  - Contextualisation and outreach (illustrative and comparative information between areas).

- **Not recommended for:**  
  - Legal/cadastral delineations or administrative/judicial decisions.  
  - Operational use requiring the **exact trunk location** (e.g., high-precision forest inventories, felling/pruning, tree-by-tree interventions) without field verification.  
  - Precise estimation of **true abundance** or **mortality** without updates/ground truthing.

**Specific limitations:**  
Photo-interpretation has limitations that can only be resolved through ground truthing; dense stands of strawberry tree (_Arbutus unedo_) and mature wild pear (_Pyrus bourgaeana_) may be confused with cork oaks in orthophotos. Moreover, although the main mortality event occurred during 2023, many individuals were already weakened in 2022 and may not have been correctly identified, or their vital status may have changed shortly afterwards. Consequently, this layer should be considered **orientative**, and detailed applications require **field confirmation**.

---

## 10. Recommended citation

M. de Felipe (2026). Updated Map of Doñana National Park. Zenodo. [DOI: https://doi.org/10.5281/zenodo.18109683](https://doi.org/10.5281/zenodo.18109683)

---

## 11. Layer change log

- **v1.0.0 (10-01-2026)** — File creation
  <!--
   **vX.Y.Z (YYYY-MM-DD)** — … -->

---

## 12. Contact

For questions, suggestions, issues, or access to non-public layers, contact me [here](mailto:m.defelipe.t@gmail.com).

---
