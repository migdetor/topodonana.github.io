---
layout: default
title: "Hidromets"
permalink: /es/content/hidromet/
menu:
  - label: "Inicio"
    url: "/es/"
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
  - label: "Google Scholar"
    url: "https://scholar.google.com/citations?user=JQzRGw4AAAAJ&hl=es"
  - label: "Contact me/ Contáctame"
    url: "mailto:m.defelipe.t@gmail.com"

citation_label: "Cita recomendada:"
citation_text: "M. de Felipe (2026). Mapa actualizado del Parque Nacional de Doñana. Zenodo."
citation_doi_label: "DOI: https://doi.org/10.5281/zenodo.18109683"
citation_doi_url: "https://doi.org/10.5281/zenodo.18109683"

---

**EN CONSTRUCCIÓN**

# Estaciones hidrometeorológicas (HIDROMET, ICTS-RBD) — Ficha de capa

>**Fuente (consulta de datos):** [HIDROMET (ICTS-RBD)](https://datos-automaticos.icts.ebd.csic.es/es/)  
>**Documentación técnica (PDF):** ver [documentación HIDROMET](https://datos-automaticos.icts.ebd.csic.es/es/info/).

>**Descarga:** [https://doi.org/10.5281/zenodo.18109683](https://doi.org/10.5281/zenodo.18109683).

>**Versión:** v1.0.0 · **Última actualización:** 10-01-2026  
>**Licencia:** CC BY-NC 4.0

---

## 1. Resumen

Esta capa contiene la **localización de las estaciones hidrometeorológicas** integradas en **HIDROMET**, la base de datos de la ICTS-Reserva Biológica de Doñana (ICTS-RBD) que almacena series hidrometeorológicas registradas por estaciones automáticas distribuidas en Doñana.

**Qué es HIDROMET (a nivel de datos):** según la documentación del sistema, las estaciones registran datos con alta frecuencia (p. ej., 5 minutos, *datos brutos*) y existen productos agregados (horarios, diarios, mensuales) para facilitar la consulta. La referencia primaria para variables, periodicidad, agregación, control y actualización es la propia plataforma y su documentación técnica.

**Autoría del dato (esta capa):** esta capa **no pretende ser un producto oficial de HIDROMET**. Es un **derivado cartográfico** preparado por el autor del mapa para facilitar su visualización e integración en el conjunto.

**Motivo de inclusión en este repositorio:** disponer de una capa GIS única (shapefile de puntos) para **representación** y **enlace** a la consulta oficial. Para el acceso a datos y metadatos operativos, consultar: https://datos-automaticos.icts.ebd.csic.es/es/

---

## 2. Contenido

- **Nombre de archivo:** `hidromet_estaciones.shp`   
- **Tipo de entidad:** Shapefile de puntos  
- **Qué se cartografía:** ubicación de estaciones HIDROMET en Doñana (puntos de estación)

---

## 3. Alcance espacial y temporal

- **Cobertura espacial:** Parque Nacional de Doñana / ámbito de estaciones gestionadas en HIDROMET (ICTS-RBD)  
- **Aviso:** esta capa representa **puntos de estación**; no sustituye a la consulta oficial ni implica exhaustividad fuera del conjunto de estaciones integradas en HIDROMET

---

## 4. Sistema de referencia (CRS)

- **CRS / EPSG (capa en este repositorio):** EPSG:25829 — ETRS89 / UTM zona 29N
- **Unidades:** metros (UTM)

---

## 5. Fuentes de datos

**Fuente primaria (oficial):**  
- HIDROMET (ICTS-RBD): https://datos-automaticos.icts.ebd.csic.es/es/

**Documentación técnica:**  
- Manual/Descripción HIDROMET (adjunto en este repositorio).

**Nota sobre redistribución:** esta web/repositorio ofrece una capa *de conveniencia* para integrar estaciones en el mapa; la referencia oficial de datos, variables y condiciones de uso debe tomarse de HIDROMET.

---

## 6. Flujo de trabajo (métodos)

*Este apartado describe únicamente lo realizado en este repositorio; la metodología de generación y curación de series debe consultarse en HIDROMET y su documentación técnica.*

- **Paso 1.** Identificación del conjunto de estaciones en la aplicación oficial HIDROMET.  
- **Paso 2.** Compilación de ubicaciones en una capa de puntos (shapefile).  
- **Paso 3.** Estandarización de atributos mínimos (ID, nombre, código y enlace a la consulta oficial).  
- **Paso 4.** Exportación a shapefile y publicación en el repositorio/Zenodo.

**Criterios clave (definiciones):**  
- **Inclusión/exclusión:** se incluyen únicamente estaciones integradas en HIDROMET (según plataforma y documentación).  
- **Supuestos:** el objetivo es cartográfico (localización + acceso); la validez y alcance de las series son los del sistema HIDROMET.

---

## 7. Estructura de datos y atributos

**Estaciones incluidas (según documentación HIDROMET):**  
Cancela Millán, Hondón del Burro, Lucio del Rey, Resolimán, Vetalengua, Juncabalejo, FAO y Brenes.

**Atributos de la capa (derivado cartográfico):** *(ajusta nombres de campo si difieren)*

| Campo | Tipo | Descripción |
|---|---|---|
| `id` | integer / string | Identificador interno único |
| `nombre` | string | Nombre de la estación (p. ej., *Lucio del Rey*) |
| `codigo` | string | Código/abreviatura (si aplica) |
| `url` | string | Enlace a la consulta oficial (HIDROMET) |
| `coordx` | double | Coordenada X (CRS del shapefile) |
| `coordy` | double | Coordenada Y (CRS del shapefile) |

**Valores ausentes / nulos:** `NULL`

---

## 8. Control de calidad y validación

- **Controles realizados (en esta capa):**  
  - Revisión de duplicados (un punto por estación).  
  - Verificación de CRS y coherencia espacial (puntos dentro del ámbito de Doñana).  
  - Comprobación de correspondencia *nombre–estación* con la plataforma/documentación HIDROMET.  

- **Validación (sistema oficial):** consultar documentación HIDROMET (adquisición, actualización, agregación y control).  

- **Problemas conocidos:**  
  - La capa no describe instrumentación ni variables por estación; para ello consultar HIDROMET.  
  - Si una estación se reubica, la posición deberá actualizarse conforme a la referencia oficial.  

- **Precisión posicional:** depende del origen de coordenadas usado para construir esta capa; para usos sensibles se recomienda contrastar con la ubicación mostrada en la plataforma oficial.

---

## 9. Limitaciones y uso apropiado

- **Usos recomendados:**  
  - Cartografía de síntesis (localización de estaciones) y orientación.  
  - Acceso rápido a la consulta de datos (mediante enlaces a HIDROMET).  

- **No recomendado para:**  
  - Inferir por sí sola series, variables, calibración o comparabilidad entre estaciones sin acudir a HIDROMET.  
  - Interpretaciones sin atender a frecuencia de muestreo, agregación y procedimientos descritos en la documentación.

---

## 10. Citación

**Cita recomendada (capa cartográfica del repositorio):**  
M. de Felipe (2026). *Mapa actualizado del Parque Nacional de Doñana* (v1.0). Zenodo. DOI: https://doi.org/10.5281/zenodo.18109683

**Cita recomendada (fuente oficial de datos):**  
HIDROMET (ICTS-RBD): https://datos-automaticos.icts.ebd.csic.es/es/  
*(Si la plataforma proporciona una referencia bibliográfica formal o DOI específico, sustitúyelo aquí.)*

---

## 11. Historial de cambios (en este repositorio)

- **v1.0.0 (10-01-2026)** — Creación de la capa de estaciones HIDROMET (shapefile de puntos) y publicación en el repositorio.

---

## 12. Contacto

Para dudas sobre esta capa (localización, atributos, enlaces): contáctame **[aquí](mailto:m.defelipe.t@gmail.com)**.  
Para cuestiones oficiales sobre la plataforma y las series: consultar la información disponible en HIDROMET.
