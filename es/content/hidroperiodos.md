---
layout: default
title: "Hidroperiodos"
permalink: /es/content/hidroperiodos/
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

# Hidroperiodos - Ficha de capa

> **Fuente metodológica / protocolo:** Laboratorio de SIG y Teledetección (LAST-EBD, CSIC), siguiendo el enfoque de reconstrucción de inundación e hidroperiodo a partir de series Landsat descrito por [Díaz-Delgado et al. (2016)](https://www.mdpi.com/2072-4292/8/9/775).
> **Descarga:** *[Zenodo](https://doi.org/10.5281/zenodo.18109683)*.
 
> **Versión:** v1.0.0 · **Última actualización:** 10-01-2026  
> **Licencia:** CC BY-NC 4.0

---

## 1. Resumen
Estas capas representan el **hidroperiodo** (duración anual de la inundación) en Doñana a partir de imágenes Landsat, expresado en categorías de días inundados por año. El hidroperiodo se entiende como la longitud de tiempo que un punto de la marisma o laguna permanece inundado a lo largo del ciclo anual (del 1 de septiembre al 31 de agosto del), derivado de máscaras binarias de inundación aplicadas a una serie temporal de escenas Landsat y posteriormente agregadas por ciclo hidrológico.

En este repositorio se distribuyen dos productos distintos, concebidos para reflejar dinámicas “representativas” de cada subsistema:
- **Lagunas**: *año de referencia 2003* (considerado “normal” en cuanto a precipitación para la dinámica lagunar).
- **Marisma**: *año de referencia 2017* (considerado “normal” para la dinámica marismeña).

Los ráster originales (hidroperiodo en cada píxel de 30x30m) fueron *poligonizados* y reclasificados en 6 clases de duración de inundación anual:
*0–60 días, 61–120, 121–180, 181–240, 241–300 o 301–365 días*.

**Autoría del dato**: el producto cartográfico (polígonos por clases) ha sido preparado por el autor del mapa a partir de productos ráster de hidroperiodo generados mediante el protocolo Landsat empleado por LAST-EBD (CSIC). 

> *Nota ecológica:* muchas lagunas efímeras pueden no inundarse o hacerlo muy brevemente en años medios; su señal espacial puede emerger con claridad únicamente en años húmedos. Por ello, estas capas deben interpretarse como una instantánea representativa del hidroperiodo para los años elegidos, no como un inventario exhaustivo de todas las lagunas inundables. Para esto último, consultar la [cartografía de lagunas]({{ "/es/content/lagunas/" | relative_url }}).

---

## 2. Contenido

Este apartado incluye dos capas vectoriales (polígonos), derivadas de ráster de hidroperiodo:

### 2.1. Hidroperiodo — Lagunas (año de referencia 2003)
- **Nombre de archivo:** hidroperiodo_lagunas_2003_25829.shp
- **Tipo de entidad:** Shapefile de polígonos
- **Qué se cartografía:** clases de duración de inundación anual asociadas a lagunas (arenas) para el año 2003.

### 2.2. Hidroperiodo — Marisma (año de referencia 2017)
- **Nombre de archivo:** hidroperiodo_marisma_2017_25829.shp (ajusta al nombre real)
- **Tipo de entidad:** Shapefile de polígonos
- **Qué se cartografía:** clases de duración de inundación anual en la marisma para el año 2017.

---

## 3. Alcance espacial y temporal

**Cobertura espacial:** Parque Nacional de Doñana y áreas cartografiadas en el mapa (según recorte aplicado al producto).
**Cobertura temporal:**
*Lagunas:* 2003 (año de referencia).
*Marisma:* 2017 (año de referencia).
**Definición temporal del hidroperiodo:** duración anual en días por ciclo; el cálculo clásico del hidroperiodo a partir de series Landsat se apoya en máscaras de inundación y un ciclo anual definido (que abarca desde el 1 de septiembre hasta el 31 de agosto).

---

## 4. Sistema de referencia (CRS)

- **CRS / EPSG:** EPSG:25829 — ETRS89 / UTM zona 29N
- **Unidades:** metros (UTM)

---
<!--
## 5. Fuentes de datos
Imágenes base: Landsat (series temporales; resolución 30 m). 
remotesensing-08-00775-v2
Protocolo / referencia metodológica: Díaz-Delgado et al., Long-Term Monitoring of the Flooding Regime and Hydroperiod of Doñana Marshes with Landsat Time Series (1974–2014). 
remotesensing-08-00775-v2
Producción / enfoque aplicado: procedimiento de discriminación de áreas inundadas a partir de umbrales y generación de máscaras de inundación por escena, agregadas para reconstruir hidroperiodo por píxel. 
remotesensing-08-00775-v2

---

## 6. Flujo de trabajo (métodos)
Cálculo del hidroperiodo por píxel (30 × 30 m) a partir de imágenes Landsat y máscaras binarias de inundación, siguiendo el protocolo descrito por Díaz-Delgado et al. 
remotesensing-08-00775-v2
Selección de un año de referencia considerado representativo:
Lagunas: 2003
Marisma: 2017
Reclasificación del ráster de hidroperiodo a 6 intervalos (0–60 … 301–365 días).
Poligonización del ráster reclasificado, generando polígonos por clase.
Estandarización y exportación a shapefile en EPSG:25829.

---
-->
## 7. Estructura de datos y atributos
### Campos del producto empleado en el proyecto

**Nombre:** 'pondhydroperiod_y2003_25829.shp' and 'marshhydroperiod_y2017_25829.shp' 

| Campo | Tipo | Descripción |
|---|---|---|
| `fid` | integer	| Identificador interno |
| `class`	| string / integer	| Clase de hidroperiodo (integer1–6) |
| `dias_min`	| integer	| Límite inferior del rango |
| `dias_max`	| integer	| Límite superior del rango |
| `anio_ref`	| integer	| Año de referencia (2003 o 2017) |
| `area` |  integer | Superficie ocupada por cada clase de hidroperiodo (en hectáreas) |

---
<!--
## 8. Control de calidad y validación

**Controles realizados:**
Consistencia espacial (CRS único EPSG:25829 y recorte/coherencia de extensión).
Coherencia de clases: verificación de que las 6 categorías están presentes y correctamente codificadas.
Revisión visual: comprobación de artefactos típicos de poligonización (polígonos muy pequeños, “islas” espurias, bordes ruidosos).
Validación:
La validación primaria corresponde a la metodología Landsat y a su calibración/contraste con observaciones in situ descrita en la literatura del protocolo (campañas de verdad-terreno, comparación con escalas limnimétricas, etc.). 

Este repositorio distribuye una derivación cartográfica (polígonos por clases) orientada a visualización y análisis a escala de mapa.

**Problemas conocidos:**
Incertidumbre temporal: un solo año de referencia no captura la variabilidad interanual (años húmedos vs. secos).
Lagunas efímeras: pueden quedar infrarrepresentadas en años medios si no llegan a inundarse.
Efectos de resolución (30 m): bordes de inundación y cubetas pequeñas pueden estar simplificados o mezclados por el tamaño de píxel. 
remotesensing-08-00775-v2
Precisión posicional:
La geometría está condicionada por la resolución Landsat y el procesamiento; el uso a escalas finas o para delimitaciones precisas requiere fuentes de mayor resolución o verificación específica.

---
-->

## 9. Limitaciones y uso apropiado

**Usos recomendados:**
Cartografía de síntesis del gradiente de inundación (hidroperiodo) en lagunas y marisma.
Contextualización ecológica (hábitats asociados a distinta permanencia de agua).
Análisis exploratorio y comparativo (p. ej., superposición con vegetación, topónimos, infraestructura, etc.) a escala compatible con resolución.

**No recomendado para:**
Delimitaciones legales/jurídicas o decisiones operativas que requieran precisión métrica fina.
Inferir la presencia/ausencia de agua en años distintos al de referencia sin considerar la variabilidad climática e hidrológica.
Diagnóstico de lagunas pequeñas o elementos lineales estrechos (caños/arroyos menores) si están por debajo de la resolución efectiva.

---

## 10. Citación
Cita recomendada (repositorio / mapa):
M. de Felipe (2026). Mapa actualizado del Parque Nacional de Doñana (v1.0). Zenodo. DOI: https://doi.org/10.5281/zenodo.18109683

Cita metodológica (protocolo Landsat-hidroperiodo):
Díaz-Delgado, R., Aragonés, D., Afán, I., & Bustamante, J. (2016). Long-Term Monitoring of the Flooding Regime and Hydroperiod of Doñana Marshes with Landsat Time Series (1974–2014). Remote Sensing, 8, 775. 

---

## 11. Historial de cambios (en este repositorio)
v1.0.0 (10-01-2026) — Publicación de capas poligonizadas por clases de hidroperiodo para: (i) lagunas (año 2003) y (ii) marisma (año 2017), derivadas de ráster.

---

## 12. Contacto
Para dudas, correcciones o sugerencias, contáctame [aqui.](mailto:m.defelipe.t@gmail.com)


