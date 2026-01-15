---
layout: default
title: "Pond cartography"
permalink: /en/content/lagunas/
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

# Cartography of the Doñana pond network — Layer factsheet

> **Official source (metadata + download):** [REDIAM record](https://portalrediam.cica.es/geonetwork/srv/api/records/db48f197-a17f-4f86-9e66-447da049f18c)  
> **Download (in this repository):** *[Zenodo](https://doi.org/10.5281/zenodo.18109683)*.
>
> **Version:** v1.0.0 · **Last updated:** 10-01-2026  
> **License:** CC BY-NC 4.0
>
> **Terms of use:** please consult the restrictions/conditions stated in the official REDIAM record.

<figure style="margin: 0 0 1rem 0;">
  <img src="{{ "/assets/img/sopeton_red.jpeg" | relative_url }}" alt="Topo Doñana" style="max-width: 100%; height: auto;">
  <figcaption style="font-size: 0.78em; opacity: 0.85; margin-top: 0.35rem; text-align: justify; text-justify: inter-word;">
In the center of the photo, Laguna del Sopetón can be seen overflowing toward the marsh. In the background on the right: Laguna del Rincón Guerrero. Photograph: Miguel de Felipe. 
  </figcaption>
</figure>

---

## 1. Summary

This layer contains the vector delineation of **temporary ponds** in Doñana National Park, distributed by the Regional Government of Andalusia through **REDIAM**. The original product includes its own metadata record and associated documentation.

**Data authorship:** this layer was not produced by the author of this website, but by *C. Gómez-Rodríguez, C. Díaz-Paniagua & J. Bustamante (2011)*.

**Reason for inclusion in this repository:** a copy is provided to facilitate centralized download within the project, always referring users to the official REDIAM record as the primary reference for metadata, scope, and conditions.

---

## 2. Content

- **Layer name (REDIAM):** Cartografía de las lagunas temporales del Parque Nacional de Doñana  
- **Feature type:** Polygons  
- **What is mapped:** temporary ponds in Doñana National Park.

---

## 3. Spatial and temporal extent

- **Spatial coverage:** Doñana National Park.  
- **Temporal reference (product):** maximum inundation in spring 2004; consult the associated documentation in REDIAM (methodology and reference dates).  
- **Recommended scale/use:** consult the official REDIAM record.

---

## 4. Coordinate reference system (CRS)

- **CRS / EPSG (according to REDIAM):** EPSG 25829 / ETRS89 UTM zone 29N (EPSG:23030 in REDIAM)  
- **Units:** meters.

---

## 5. Data sources

**Primary (official) source:**  
- *Gómez-Rodríguez, C., Díaz-Paniagua, C. & Bustamante, J. (2011). Cartografía de las lagunas temporales del Parque Nacional de Doñana. Agencia Andaluza del Agua. Consejería de Medio Ambiente. Junta de Andalucía.*

**Associated documentation (available in REDIAM):**  
- *Geographic Data Model* (field and type structure).  
- Product report(s)/memorandum (methodology, scope, limitations).

**Redistribution note:** this website/repository provides a “convenience copy” for download within the project; the official reference for metadata and restrictions should be taken from the REDIAM record.

---

## 6. Workflow (methods)

*Not applicable.*

---

## 7. Data structure and attributes (according to REDIAM)

### Fields used in this project

**Name:** `pondcartography_25829.shp`

| Field | Type | Description |
|---|---|---|
| `fid` | (OID) | Internal identifier |
| `COORDX` | (Double) | X coordinate (EPSG:25829) |
| `COORDY` | (Double) | Y coordinate (EPSG:25829) |
| `AREA` | (Double) | Maximum inundation area of the pond |
| `ID_LAGTEMP` | (Double) | Pond identifier/code |
| `TOPONIMO` | (String) | Pond name/toponym |

---

## 8. Quality control and validation

Please consult the associated REDIAM documentation (methodology and error assessment).

---

## 9. Limitations and appropriate use

- **Recommended uses:**  
  - Visualization and exploratory analysis at park scale.  
  - Support for field surveys and sampling planning, respecting the scale recommended by the product.

- **Not recommended for:**  
  - Legal/juridical delineations or decisions requiring fine-detail precision without specific verification.  
  - Interpretations beyond the temporal/methodological scope described in the original product.

---

## 10. Citation

**Recommended citation:**  
Gómez-Rodríguez, C., Díaz-Paniagua, C. & Bustamante, J. (2011). *Cartografía de las lagunas temporales del Parque Nacional de Doñana*. Agencia Andaluza del Agua. Consejería de Medio Ambiente. Junta de Andalucía.

Record: [https://portalrediam.cica.es/geonetwork/srv/api/records/db48f197-a17f-4f86-9e66-447da049f18c](https://portalrediam.cica.es/geonetwork/srv/api/records/db48f197-a17f-4f86-9e66-447da049f18c)

---

## 11. Change history (in this repository)

- **v1.0.0 (10-01-2026)** — Inclusion of a copy of the REDIAM product and a version with minimal attributes (no geometric modification).

---

## 12. Contact

For questions about the project repository: contact me [here](mailto:m.defelipe.t@gmail.com)  
For official questions about metadata/distribution of the dataset: see the contact details in the REDIAM record.
