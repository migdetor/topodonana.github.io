---
layout: default
title: "Hidromets"
permalink: /es/content/hidromet/
menu:
  - label: "Inicio"
    url: "/es/"
  - label: "Doñana"
    url: "/es/doniana/"
  - label: "Justificación"
    url: "/es/preface/"
  - label: "El mapa"
    url: "/es/map/"
  - label: "Información cartográfica"
    url: "/es/content/"
  - label: "Descarga de datos"
    url: "https://doi.org/10.5281/zenodo.18109683"
  - label: "Recursos adicionales"
    url: "/es/recursos/"

links:
  - label: "Contact me/ Contáctame"
    url: "/contact/"

citation_label: "Reccomended citation - Cita recomendada:"
citation_text: "M. de Felipe (2026). Mapa actualizado del Parque Nacional de Doñana (v1.0). Zenodo."
citation_doi_label: "DOI: [DOI]"
citation_doi_url: "https://doi.org/10.5281/zenodo.18109683"

---

# Estaciones hidrometeorológicas (ICTS-RBD) — Ficha de capa

>**Fuente (consulta de datos):** [HIDROMET (ICTS-RBD)](https://datos-automaticos.icts.ebd.csic.es/es/)  
>**Documentación técnica (PDF):** ver [documentación HIDROMET](https://datos-automaticos.icts.ebd.csic.es/es/info/).

>**Descarga:** [https://doi.org/10.5281/zenodo.18109683](https://doi.org/10.5281/zenodo.18109683).

>**Versión:** v1.0.0 · **Última actualización:** 10-01-2026  
>**Licencia:** CC BY-NC 4.0

---

## 1. Resumen

Esta capa contiene la **localización de las estaciones hidrometeorológicas** integradas en **HIDROMET**, la base de datos de la **[ICTS-Reserva Biológica de Doñana (ICTS-RBD)](https://icts-donana.csic.es)** que almacena series hidrometeorológicas registradas por estaciones automáticas distribuidas en Doñana.

Las estaciones Hidromet registran datos ambientales de alta frecuencia (e.g. cada 5 minutos) y de forma agregada (horarios, diarios, mensuales). Para más información acerca de las variables ambientales medidas por cada estación, periodicidad, agregación, control y actualización, consulten [la propia plataforma y su documentación técnica](https://datos-automaticos.icts.ebd.csic.es/es/).

**Autoría del dato:** esta capa **no pretende ser un producto oficial de HIDROMET**. Es un **derivado cartográfico** preparado por el autor del mapa para facilitar su visualización e integración en el conjunto.

**Motivo de inclusión en este repositorio:** disponer de una capa GIS única (shapefile de puntos) para **representación** y **[enlace](https://datos-automaticos.icts.ebd.csic.es/es/)** a la consulta oficial. Para el acceso a datos y metadatos operativos, consultar: [https://datos-automaticos.icts.ebd.csic.es/es/]((https://datos-automaticos.icts.ebd.csic.es/es/))

---

## 2. Contenido

- **Nombre de archivo:** `hidromet_25829.shp`   
- **Tipo de entidad:** Shapefile de puntos  
- **Qué se cartografía:** ubicación de estaciones HIDROMET en Doñana (puntos de estación)

---

## 3. Alcance espacial y temporal

- **Cobertura espacial:** Parque Nacional de Doñana / ámbito de estaciones gestionadas en HIDROMET (ICTS-RBD)
>>**Aviso:** esta capa representa **puntos de estación**; no sustituye a la consulta oficial ni implica exhaustividad fuera del conjunto de estaciones integradas en HIDROMET

---

## 4. Sistema de referencia (CRS)

- **CRS / EPSG (capa en este repositorio):** EPSG:25829 — ETRS89 / UTM zona 29N
- **Unidades:** metros (UTM)

---

## 5. Fuentes de datos

**Fuente primaria (oficial):**  
- HIDROMET (ICTS-RBD): https://datos-automaticos.icts.ebd.csic.es/es/

**Nota sobre redistribución:** esta web/repositorio ofrece una capa *de conveniencia* para integrar estaciones en el mapa; la referencia oficial de datos, variables y condiciones de uso debe tomarse de HIDROMET.

---

## 6. Flujo de trabajo (métodos)

*No aplica.*

---

## 7. Estructura de datos y atributos

**Estaciones incluidas (según documentación HIDROMET):**  
Cancela Millán, Hondón del Burro, Lucio del Rey, Resolimán, Vetalengua, Juncabalejo, FAO y Brenes.

**Atributos de la capa (derivado cartográfico):** *(ajusta nombres de campo si difieren)*

| Campo | Tipo | Descripción |
|---|---|---|
| `id` | integer / string | Identificador interno único |
| `nombre` | string | Nombre de la estación (p. ej., *Lucio del Rey*) |
| `coordx` | double | Coordenada X (CRS del shapefile) |
| `coordy` | double | Coordenada Y (CRS del shapefile) |

**Valores ausentes / nulos:** `NULL`

---

## 8. Control de calidad y validación
Consultar la documentación asociada en [HIDROMET (ICTS-RBD)](https://datos-automaticos.icts.ebd.csic.es/es/)

---

## 9. Limitaciones y uso apropiado

- **Usos recomendados:**  
  - Cartografía de síntesis (localización de estaciones) y orientación.  
  - Acceso rápido a la consulta de datos (mediante enlaces a HIDROMET).
  - Apoyo a prospecciones y planificación de muestreo, manteniendo la escala recomendada por el producto. 

- **No recomendado para:**  
  - Delimitaciones legales/jurídicas o decisiones que requieran precisión de detalle sin verificación específica.
  - Interpretaciones fuera del alcance temporal/metodológico descrito en el producto original.

---

## 10. Citación

**Cita recomendada (capa cartográfica del repositorio):**  
M. de Felipe (2026). *Mapa actualizado del Parque Nacional de Doñana* (v1.0). Zenodo. DOI: https://doi.org/10.5281/zenodo.18109683

**Cita recomendada (fuente oficial de datos):**  
HIDROMET (ICTS-RBD): https://datos-automaticos.icts.ebd.csic.es/es/ 

---

## 11. Historial de cambios (en este repositorio)

- **v1.0.0 (10-01-2026)** — Creación de la capa de estaciones HIDROMET (shapefile de puntos) y publicación en el repositorio.

---

## 12. Contacto

Para dudas sobre esta capa (localización, atributos, enlaces): contáctame **[aquí](mailto:m.defelipe.t@gmail.com)**.  
Para cuestiones oficiales sobre la plataforma y las series: consultar la información disponible en HIDROMET.
