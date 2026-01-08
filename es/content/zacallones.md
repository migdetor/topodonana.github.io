---
layout: default
title: "Zacallones"
permalink: /es/content/zacallones/
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

# Zacallones, pozos y ojos — Ficha de capa

**Descarga:** *[Zenodo](https://doi.org/10.5281/zenodo.18109683)*.

**Versión:** v1.0.0 · **Última actualización:** 10-01-2026  
**Licencia:** CC BY-NC 4.0  

---

## 1. Resumen

Esta capa recoge la localización de **zacallones**, **pozos**, **abrevaderos** y **ojos** del Parque Nacional de Doñana, en formato de puntos, con fines cartográficos, orientativos y de apoyo del territorio.

En el área de Doñana, el término **zacallón** es una variante popular de *azacaya* (con aféresis y el sufijo aumentativo *-ón*). *Azacaya* es una voz de origen árabe asociada a *conductos o ramales de agua* y, en Doñana, se emplea con valor toponímico y apelativo para referirse a **aguas provenientes de un ojo, donde el ganado abreva**. *(DRAE, s.v.; Castrillo Díaz 1994).*  

Los **ojos** son **afloramientos de agua dulce** vinculados al acuífero confinado bajo el terreno arcilloso de la marisma. Tienen un alto valor ecológico al constituir una de las **escasas fuentes de agua dulce durante el verano**, especialmente en años secos.

**Autoría del dato:** esta capa parte de una base previa del **equipo de Seguimiento** de la **ICTS Doñana**, que ha sido **revisada, ampliada y actualizada por el autor** para reflejar el estado actual del Parque. En el proceso se han eliminado elementos ya desaparecidos, corregido localizaciones y añadido nuevos puntos que no estaban reflejados.

**Motivo de inclusión en este repositorio:** disponer de una capa GIS única y actualizada que integre, de manera coherente con el mapa, estos elementos hidráulicos y toponímicos, permitiendo su visualización conjunta y su trazabilidad en futuras versiones.

> **Aviso:** capa orientativa. No es un inventario oficial de infraestructuras hidráulicas ni debe emplearse para usos administrativos, legales o de gestión operativa sin verificación específica.

---

## 2. Contenido

- **Nombre de archivo:** `zacallones_pozos_ojos_25829.shp` *(ajusta al nombre real)*  
- **Tipo de entidad:** Shapefile de puntos  
- **Qué se cartografía:** localización de zacallones, pozos, abrevaderos y ojos en Doñana.

---

## 3. Alcance espacial y temporal

- **Cobertura espacial:** Parque Nacional de Doñana y *marisma gallega* del Parque Natural.
- **Cobertura temporal (referencia):** actualización basada en revisión y fotointerpretación realizada hasta **2025**.
- **Aviso:** algunos elementos pueden haber cambiado con el tiempo (colmatación, abandono, destrucción, restauraciones), especialmente en infraestructuras menores.

---

## 4. Sistema de referencia (CRS)

- **CRS / EPSG (capa en este repositorio):** EPSG:25829 — ETRS89 / UTM zona 29N  
- **Unidades:** metros (UTM)

---

## 5. Fuentes de datos

**Base de partida:**  
- Base previa del equipo de seguimiento de la **ICTS Doñana**.

**Tratamiento posterior:**  
- La base fue **modificada, revisada, ampliada y actualizada por el autor** (Sección 6), mediante fotointerpretación y consultas.

---

## 6. Flujo de trabajo (métodos)

- **Paso 1. Revisión y depuración de la base de partida (ICTS Doñana)**  
  Se examinó la coherencia espacial y la duplicidad de registros. Se identificaron puntos con incertidumbre o potencial obsolescencia (elementos ausentes o transformados).

- **Paso 2. Verificación por fotointerpretación**  
  Se comprobó, mediante ortofotografía de alta resolución, la presencia/ausencia de elementos (especialmente pozos, abrevaderos y estructuras asociadas), corrigiendo localizaciones cuando fue necesario y eliminando puntos sin evidencia actual.

- **Paso 3. Ampliación y actualización mediante consultas locales y expertas**  
  Se incorporaron nuevos puntos no incluidos en la base inicial a partir de **consultas con expertos y personas conocedoras del territorio**, priorizando la coherencia toponímica y el conocimiento de usos tradicionales.

- **Paso 4. Estandarización y exportación**  
  Se homogenizaron campos, codificación y formato. Se exportó el producto final como shapefile en EPSG:25829.

**Criterios clave (definiciones):**  
- **Inclusión/exclusión:** se incluyen elementos hidráulicos/to-ponímicos identificables (por evidencia en ortofoto y/o confirmación por conocimiento local/experto). Se excluyen puntos cuya existencia actual no puede sostenerse con la evidencia disponible.  
- **Supuestos:** la fotointerpretación permite una verificación razonable para cartografía de síntesis, pero no reemplaza la verificación en campo en elementos pequeños o cubiertos por vegetación.

---

## 7. Estructura de datos y atributos

| Campo | Tipo | Descripción |
|---|---|---|
| `id` | integer / string | Identificador interno único |
| `tipo` | string | Tipo de elemento (`zacallon`, `pozo`, `abrevadero`, `ojo`) |
| `status` | string | Tipo de elemento (`degraded`, `good`, `NULL`) |
| `nombre` | string | Nombre/topónimo (si existe) |
| `coordx` | double | Coordenada X (en CRS del shapefile) |
| `coordy` | double | Coordenada Y (en CRS del shapefile) |

**Valores ausentes / nulos:** `NULL`

---

## 8. Control de calidad y validación

- **Controles realizados:**  
  - Revisión de duplicados y consistencia espacial (CRS EPSG:25829).  
  - Inspección visual por fotointerpretación de puntos críticos o dudosos.  
  - Homogeneización de tipologías y codificación de atributos.

- **Validación:**  
  - Contraste entre base de partida (ICTS Doñana), fotointerpretación y consultas expertas/locales.  
  - La validación exhaustiva requeriría verificación de campo sistemática.

- **Problemas conocidos:**  
  - **Detectabilidad limitada** por cobertura vegetal, sombra o tamaño reducido de infraestructuras.  
  - **Incertidumbre temporal:** algunos puntos pueden variar rápidamente (colmatación, restauración, abandono).  
  - **Toponimia variable:** un mismo elemento puede tener variantes locales de nombre.

- **Precisión posicional:**  
  Orientativa. Para usos sensibles a posición exacta se recomienda verificación en campo o contraste con fuentes oficiales.

---

## 9. Limitaciones y uso apropiado

- **Usos recomendados:**  
  - Cartografía de síntesis y contextualización ecológica y cultural del territorio.  
  - Apoyo orientativo para prospección y trabajo de campo (a escala de parque).  
  - Análisis exploratorio de patrones espaciales a escala compatible con la resolución del producto.

- **No recomendado para:**  
  - Decisiones administrativas/jurídicas o inventarios operativos sin verificación de campo.  
  - Uso que requiera localización exacta o caracterización funcional actual (estado, caudal, accesibilidad).

**Limitaciones específicas:**  
- La fotointerpretación y las consultas mejoran la base, pero no garantizan exhaustividad ni permanencia temporal. Esta capa debe entenderse como una representación **orientativa y actualizable**.

---

## 10. Citación

**Cita recomendada:**  
M. de Felipe (2026). *Mapa actualizado del Parque Nacional de Doñana* (v1.0). Zenodo. DOI: https://doi.org/10.5281/zenodo.18109683

---

## 11. Historial de cambios (en este repositorio)

- **v1.0.0 (10-01-2026)** — Revisión, ampliación y actualización de la base de zacallones, pozos, abrevaderos y ojos (derivada de una base previa de ICTS Doñana), mediante fotointerpretación y consultas.

---

## 12. Contacto

Para dudas, correcciones o aportes (p. ej., existencia actual, nombre local, nuevas localizaciones): contáctame **[aquí](mailto:m.defelipe.t@gmail.com)**.
