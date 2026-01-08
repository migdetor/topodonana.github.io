---
layout: default
title: "Toponimos"
permalink: /es/content/toponimos/
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

# Toponimia — Ficha de capa

**Descarga:** [Zenodo](https://doi.org/10.5281/zenodo.18109683).

**Versión:** v1.0.0 · **Última actualización:** 10-01-2026  
**Licencia:** CC BY-NC 4.0  

---

## 1. Resumen

Esta capa recoge la **toponimia histórica y actual** del Parque Nacional de Doñana y su entorno inmediato, con fines **cartográficos, culturales y de interpretación socio-ecológica** del territorio. 

El núcleo de la capa parte de los **topónimos empleados por J. Castroviejo (1993)** en el *Mapa del Parque Nacional de Doñana*, que han sido **extraídos manualmente** y posteriormente **comprobados, corregidos, ampliados y jerarquizados**. El objetivo es conservar la coherencia con la toponimia fundacional del mapa de referencia, pero dotándola de una estructura operativa que permita distinguir tipos de lugar, escala y permanencia en el paisaje.

**Autoría del dato:** esta capa ha sido **compilada y editada por el autor** a partir de la cartografía de Castroviejo (1993), conocimiento personal del territorio, recopilación de fuentes históricas (memorias, libros, cartografía previa) y consultas con personas del entorno y expertos.

**Carácter vivo:** la capa se encuentra en **revisión y mejora continua**, incorporando nuevos topónimos y ajustando nombres, categorías y localizaciones cuando se detecten errores o se obtenga nueva información.

---

## 2. Contenido

El dataset se distribuye en **dos capas**:

### 2.1. Toponimia puntual (puntos)
- **Nombre de archivo:** `toponimia_25829.shp`
- **Tipo de entidad:** Shapefile de **puntos**  
- **Qué se cartografía:** topónimos representables mediante un punto cartográfico (incluye también nombres de “zona” o “finca” representados por un punto de referencia).

### 2.2. Toponimia lineal (líneas)
- **Nombre de archivo:** `toponimia_lineal_25829.shp`  
- **Tipo de entidad:** Shapefile de **líneas**  
- **Qué se cartografía:** formas lineales (principalmente **arroyos**, **caños** y otros elementos hidrológicos lineales) cuyos nombres no se representan adecuadamente como punto.

---

## 3. Alcance espacial y temporal

- **Cobertura espacial:** Parque Nacional de Doñana y zonas aledañas incluidas en el mapa (según composición cartográfica del proyecto).  
- **Cobertura temporal (referencia):** la capa integra toponimia histórica (Castroviejo 1993) y toponimia vigente (según fuentes actuales y conocimiento local).  
> **Aviso:** la toponimia puede cambiar por usos locales, variaciones fonéticas, oficialización administrativa o transformación del paisaje (pérdida de lagunas, cambio de usos, desaparición de edificaciones).

---

## 4. Sistema de referencia (CRS)

- **CRS / EPSG (capas en este repositorio):** EPSG:25829 — ETRS89 / UTM zona 29N  
- **Unidades:** metros (UTM)

---

## 5. Fuentes de datos

**Base de partida (toponimia de referencia):**  
- Castroviejo, J. (1993). *Mapa del Parque Nacional de Doñana* *(ajusta la cita completa según tu bibliografía)*.

**Tratamiento posterior:**  
- La base fue **extraída manualmente** y posteriormente **corregida, ampliada y jerarquizada por el autor** (Sección 6).

**Fuentes complementarias:**  
- Fuentes históricas (libros, memorias, cartografía previa).  
- Consultas con personas locales y expertas.  
- Conocimiento personal del territorio.

> Nota: dada la naturaleza cultural y oral de parte de la toponimia, algunas entradas pueden tener variantes de grafía, pronunciación o uso local.

---

## 6. Flujo de trabajo (métodos)

- **Paso 1. Extracción manual de la base toponímica (Castroviejo 1993)**  
  Se transcribieron los topónimos del mapa original y se asignó una localización para su representación una vez comprobada su veracidad.

- **Paso 2. Revisión, corrección y estandarización**  
  Se revisaron grafías, duplicidades y coherencia interna (términos repetidos, variantes), estandarizando formato y campos.

- **Paso 3. Ampliación de topónimos y contraste de fuentes**  
  Se incorporaron topónimos adicionales procedentes de fuentes históricas, bibliografía y consultas locales/expertas, manteniendo trazabilidad conceptual con el mapa de referencia.

- **Paso 4. Jerarquización y clasificación temática**  
  Se definieron categorías operativas para distinguir escala y naturaleza del topónimo (ver Sección 7), incluyendo la distinción hidrológica entre **arenas** y **marisma**.

- **Paso 5. Representación geométrica (puntos y líneas)**  
  - Se representaron como **puntos** los topónimos no lineales (incluyendo zonas/fincas mediante un punto representativo).  
  - Se representaron como **líneas** los elementos claramente lineales (arroyos, caños y similares).

---

## 7. Estructura de datos y atributos

### 7.1. Atributos (capa de puntos)

| Campo | Tipo | Descripción |
|---|---|---|
| `fid` | (OID) / integer | Identificador interno |
| `categoria` | string | Categoría jerárquica del topónimo *(ver abajo)* |
| `nombre` | string | Nombre/topónimo |
| `tipo` | string | Tipo temático (p. ej., hidrología/arenas/marisma, edificación, finca, etc.) |
| `coordx` | double | Coordenada X (CRS del shapefile) |
| `coordy` | double | Coordenada Y (CRS del shapefile) |

**Categorías empleadas (`categoria`)** *(según tu definición actual):*  
- `hito` (hitos/puntos concretos; p. ej., *Alcornoque Escobar*, *Alameda de Alcuña*)  
- `zona` (unidad espacial; p. ej., *Corral Mahón*)  
- `finca` (unidad espacial amplia tradicional; p. ej., *El Puntal*)  
- `edificacion` (construcciones; p. ej., *Palacio de Doñana*)  
- `desaparecido` (lugares desaparecidos; p. ej., *Laguna del Brezo*, *Casa de Marilópez*)  
- `hidrologia` (topónimos hidrológicos; ver `tipo` para arenas/marisma)

**Valores ausentes / nulos:** `NULL`

**Criterios clave (definiciones):**  
- **Zonas y fincas:** aunque se representen con coordenadas puntuales, se entienden como **unidades espaciales extensas**; el punto actúa como referencia cartográfica, no como localización exacta.  
- **Lugares desaparecidos:** topónimos asociados a elementos ya inexistentes por cambios ecológicos o humanos (p. ej., desecación de lagunas, derribo de edificaciones).  
- **Hidrología:** se distingue entre nombres asociados a sistemas de **arenas** (lagunas, arroyos, caños arenosos) y nombres propios de la **marisma** (caños, lucios, ojos, etc., cuando aplica).

### 7.2. Atributos (capa de líneas)


| Campo | Tipo | Descripción |
|---|---|---|
| `fid` | (OID) / integer | Identificador interno |
| `categoria` | string | Categoría jerárquica del topónimo *(p. ej., `hidrologia`)* |
| `nombre` | string | Nombre/topónimo |
| `tipo` | string | Tipo temático (p. ej., `arroyo`, `caño`, `marisma`, `arenas`) |

---

## 8. Control de calidad y validación

- **Controles realizados:**  
  - Revisión de duplicidades y homogeneización de grafías (variantes locales, tildes, mayúsculas).  
  - Coherencia categorial (misma lógica para `categoria` y `tipo`).  
  - Comprobación espacial básica (topónimos dentro del ámbito del mapa y coherencia con unidades del paisaje).

- **Validación:**  
  - Contraste con el mapa de referencia (Castroviejo 1993).  
  - Verificación por conocimiento local y consultas con personas expertas/locales cuando ha sido posible.  

- **limitaciones:**  
  - **Incertidumbre espacial:** para `zona` y `finca`, el punto es representativo y no delimita el área real.  
  - **Variabilidad lingüística:** un mismo topónimo puede aparecer con variantes de pronunciación o grafía.  
  - **Cambios temporales:** algunos nombres caen en desuso, otros se oficializan o cambian con el tiempo.

- **Precisión posicional:**  
  Orientativa. No es cartografía de deslinde ni de localización legal; para usos sensibles se recomienda contraste con fuentes oficiales o verificación in situ.

---

## 9. Limitaciones y uso apropiado

- **Usos recomendados:**  
  - Cartografía de síntesis y divulgación (lectura cultural del paisaje).  
  - Soporte a trabajos de investigación o interpretación territorial que requieran una base toponímica coherente y trazable.  
  - Orientación y contextualización de capas ecológicas e históricas en el mapa.

- **No recomendado para:**  
  - Usos administrativos/jurídicos o decisiones que requieran nomenclátor oficial.  
  - Inferir límites espaciales reales a partir de puntos.  
  - Localización de detalle sin verificación específica.

---

## 10. Citación

**Cita recomendada:**  
M. de Felipe (2026). *Mapa actualizado del Parque Nacional de Doñana* (v1.0). Zenodo. DOI: https://doi.org/10.5281/zenodo.18109683

---

## 11. Historial de cambios (en este repositorio)

- **v1.0.0 (10-01-2026)** — Extracción manual de topónimos de Castroviejo (1993) y compilación ampliada (corrección, ampliación, jerarquización y clasificación; inclusión de capa lineal para arroyos y caños).

---

## 12. Contacto

Para correcciones, variantes locales, topónimos faltantes o discusión de categorías: contáctame **[aquí](mailto:m.defelipe.t@gmail.com)**.
