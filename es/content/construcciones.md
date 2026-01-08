---
layout: default
title: "Construcciones"
permalink: /es/content/construcciones/
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

# Edificaciones de interés — Ficha de capa

**Descarga:** *[Zenodo](https://doi.org/10.5281/zenodo.18109683)*.   
**Versión:** v1.0.0 · **Última actualización:** 10-01-2026  
**Licencia:** CC BY-NC 4.0  

<figure style="margin: 0 0 1rem 0;">
  <img src="{{ "/assets/img/casalosguardas_red.jpeg" | relative_url }}" alt="Topo Doñana" style="max-width: 100%; height: auto;">
  <figcaption style="font-size: 0.78em; opacity: 0.85; margin-top: 0.35rem; text-align: justify; text-justify: inter-word;">
Casa de los Guardas. Fotografía: Miguel de Felipe. 
  </figcaption>
</figure>

---

## 1. Resumen

Esta capa recoge **edificaciones y elementos construidos de interés** en el Parque Nacional de de Doñana y zonas aledañas, con fines **cartográficos, orientativos y divulgativos**. Incluye, de manera no necesariamente exhaustiva, **palacios**, **casas de guardas**, **torres vigía**, **casas cuarteles**, **faros** y **centros de visitantes**.

**Autoría del dato:** esta cartografía ha sido **creada por el autor** del mapa mediante **fotointerpretación** y conocimiento del territorio (memoria cartográfica y referencias locales), con el objetivo de integrar en una misma composición elementos que estructuran la lectura humana del paisaje.

**Motivo de inclusión en este repositorio:** disponer de una capa GIS simple que permita **localizar** estas edificaciones en el mapa, enlazarlas con otras capas temáticas y servir como base para **correcciones y mejoras** futuras por parte de personas conocedoras del territorio.

> **Aviso:** capa orientativa. No es un inventario oficial ni debe emplearse para usos administrativos, legales o catastrales.
> **Nota:** Las construcciones ya desaparecidas se encuentran reflejadas en la capa cartográfica de toponimia bajo la categoría de "lugares desaparecidos"

---

## 2. Contenido

El dataset se distribuye en **dos capas**:

### 2.1. Torres vigía y faros
- **Nombre de archivo:** `Watchtowers-Torres_25829.shp`  
- **Tipo de entidad:** Shapefile de **puntos**  
- **Qué se cartografía:** localización puntual de torres vigía y faros.

### 2.2. Edificaciones de interés
- **Nombre de archivo:** `Buildings-Costrucciones_25829.shp`
- **Tipo de entidad:** Shapefile de **polígonos**  
- **Qué se cartografía:** planta aproximada de edificaciones de interés (palacios, casas de guardas, cuarteles, centros de visitantes, etc.).

---

## 3. Alcance espacial y temporal

- **Cobertura espacial:** Parque Nacional de Doñana y elementos próximos cuando son relevantes para el conjunto cartográfico.  
- **Cobertura temporal (referencia):** digitalización realizada a partir de fotointerpretación y conocimiento del territorio disponible hasta **2025**. 
- **Aviso:** la presencia, estado o uso de algunas construcciones puede cambiar con el tiempo (derribos, ruinas, reformas, nuevos usos).

---

## 4. Sistema de referencia (CRS)

- **CRS / EPSG (capas en este repositorio):** EPSG:25829 — ETRS89 / UTM zona 29N  
- **Unidades:** metros (UTM)

---

## 5. Fuentes de datos

**Base de trabajo:**  
- Fotointerpretación propia (ortofotografía de alta resolución) y conocimiento del territorio.

**Nota:** esta capa no se apoya en un inventario institucional único. Se publica como un producto **cartográfico propio**, susceptible de mejora mediante contraste con inventarios oficiales, bibliografía histórica o verificación de campo.

---

## 6. Flujo de trabajo (métodos)

- **Paso 1. Identificación de elementos**  
  Compilación inicial de lugares y edificaciones relevantes (palacios, casas de guardas, torres vigía, cuarteles, faros, centros de visitantes) a partir de conocimiento del territorio.

- **Paso 2. Digitalización por fotointerpretación**  
  - **Torres y faros:** digitalización como **puntos** sobre el elemento identificable.  
  - **Edificaciones:** digitalización como **polígonos** siguiendo la huella visible (aproximada) en ortofoto.

- **Paso 3. Estandarización de atributos y exportación**  
  Asignación de identificadores únicos, homogeneización de campos y exportación final en CRS EPSG:25829.

**Criterios clave (definiciones):**  
- **Inclusión/exclusión:** se incluyen edificaciones claramente identificables y de relevancia cultural/funcional para la lectura del territorio; se excluyen construcciones menores no distinguibles o sin relevancia para el mapa de síntesis.  
- **Supuestos:** la ortofotografía permite una delineación aproximada suficiente para cartografía de síntesis, pero no garantiza precisión a escala de inventario.

---

## 7. Estructura de datos y atributos

### 7.1. Capa de puntos: torres vigía y faros

| Campo | Tipo | Descripción |
|---|---|---|
| `id` | integer / string | Identificador interno único |
| `name` | string | Nombre del elemento (torre/faro) |
| `coordx` | double | Coordenada X (CRS del shapefile) |
| `coordy` | double | Coordenada Y (CRS del shapefile) |

**Valores ausentes / nulos:** `NULL`

### 7.2. Capa de polígonos: edificaciones de interés

| Campo | Tipo | Descripción |
|---|---|---|
| `id` | integer / string | Identificador interno único |
| `name` | string | Nombre de la edificación *(en esta versión: `NULL`)* |
| `coordx` | double | Coordenada X (CRS del shapefile) |
| `coordy` | double | Coordenada Y (CRS del shapefile) |

**Valores ausentes / nulos:** `NULL`

> Nota: en esta versión, el campo **`nombre`** en la capa de polígonos se publica vacío (`NULL`). Queda preparado para completar nombres en futuras versiones o mediante contribuciones/correcciones.

---

## 8. Control de calidad y validación

- **Controles realizados:**  
  - Revisión visual de duplicados (un registro por elemento) y coherencia espacial.  
  - Verificación de CRS (EPSG:25829) y de que las geometrías se sitúan en el ámbito esperado.  
  - Revisión manual básica de geometrías (polígonos cerrados, sin errores evidentes).

- **Validación:**  
  Esta versión se basa principalmente en fotointerpretación y conocimiento del territorio. La validación exhaustiva requiere contraste con inventarios oficiales, bibliografía histórica o verificación de campo.

- **Precisión posicional:**  
  Orientativa. Para usos sensibles a posición exacta o límites de edificio, se recomienda verificación específica.

---

## 9. Limitaciones y uso apropiado

- **Usos recomendados:**  
  - Cartografía de síntesis y divulgación (localización de elementos construidos relevantes).  
  - Contextualización histórica y cultural del territorio en el mapa.  
  - Apoyo orientativo a prospecciones y planificación de visitas/muestreo (a escala de parque).

- **No recomendado para:**  
  - Delimitaciones legales/catastrales, planificación de obra, autorizaciones o decisiones administrativas.  
  - Interpretaciones de detalle (dimensiones exactas, límites precisos, estado de conservación) sin verificación.

**Limitaciones específicas:**  
- **No es exhaustivo** y **cambios temporales** (edificaciones derribadas, transformadas o de nuevo uso).  
- Posibles **errores de identificación** en elementos poco distinguibles o parcialmente ocultos.  
- En la capa de polígonos, el campo `nombre` está pendiente de completar en versiones futuras.

---

## 10. Citación

**Cita recomendada:**  
M. de Felipe (2026). *Mapa actualizado del Parque Nacional de Doñana* (v1.0). Zenodo. DOI: https://doi.org/10.5281/zenodo.18109683

---

## 11. Historial de cambios (en este repositorio)

- **v1.0.0 (10-01-2026)** — Creación de la capa de *edificaciones de interés* (polígonos) y *torres vigía y faros* (puntos) mediante fotointerpretación y digitalización manual.

---

## 12. Contacto

Para dudas, correcciones o sugerencias (p. ej., nombres faltantes, edificaciones no incluidas, cambios de estado): contáctame **[aquí](mailto:m.defelipe.t@gmail.com)**.
