---
layout: default
title: "Alcornoques"
permalink: /es/content/alcornoques/
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

# Alcornoques del P. N. Doñana - Ficha de capa

> **Descarga:** [Zenodo](https://doi.org/10.5281/zenodo.18109683)  
> **Versión:** v1.0.0 · **Última actualización:** 10-01-2026  
> **Licencia:** CC BY-NC 4.0

<img src="{{ "/assets/img/alcmapa.png" | relative_url }}" alt="Topo Doñana" style="max-width: 100%; height: auto; margin: 0 0 1rem 0;">

---

## 1. Resumen

El marcaje de los alcornoques centenarios fue una de las primeras labores que J. A. Valverde encomendara en 1963 a los guardas mayores Antonio Chico y José Boixo en aquella incipiente Reserva Biológica de Doñana (RBD). Los alcornoques se marcaban con tablillas marcadas al fuego con un número único y, en total, se marcaron 454 alcornoques; 136 de ellos serían fotografiados en 1966 por [Lorenzo García](https://ealorenzogarcia.wordpress.com/la-figura-de-lorenzo-garcia/), del Centro de Aclimatación de Almería (perteneciente al CSIC). Durante 1989-1990, Juan Carlos Solís elaboró la primera cartografía de los alcornoques de la RBD. Sobre esta cartografía, ya en 2008-2012, se tomó la posición GPS de los alcornoques, encontrándose 315 de ellos vivos ([Ramo & Calderon 2013](http://libros.csic.es/product_info.php?products_id=752)). Sobre esta base –y con motivo de las mortandades de alcornoques debido a su ocupación por las pajareras y la seca de encina–, la Dra. Cristina Ramo inició el seguimiento de ~250 alcornoques, incluyendo 133 alcornoques monitorizados de forma sistemática en la Reserva Biológica de Doñana y 119 monitorizados de forma puntual distribuidos a lo largo del Parque Nacional. En 2023, el mal estado del acuífero de Doñana fue responsable de que el [7% de los alcornoques de la Reserva Biológica murieran en menos de un año](https://efeverde.com/alcornoques-reserva-biologica-donana/).

<img src="{{ "/assets/img/portadaalc.png" | relative_url }}" alt="Topo Doñana" style="max-width: 100%; height: auto; margin: 0 0 1rem 0;">

Para poner en valor la abundancia y distribución de estos alcornoques centenarios, hemos recopilado y combinado bases de datos del alcornocal de la RBD y ampliado mediante fotointerpretación de ortofotografías a la **totalidad del Parque Nacional**. De este modo, se han logrado identificar un total de **2584 alcornoques** que se encontraban vivos hasta 2022.

**Descarga el catálogo fotográfico de los alcornoques de la RBD** de Ramo & Calderon (2013) [aqui](http://libros.csic.es/product_info.php?products_id=752)

<img src="{{ "/assets/img/206.jpg" | relative_url }}" alt="Topo Doñana" style="max-width: 100%; height: auto; margin: 0 0 1rem 0;">
---

## 2. Contenido

- **Nombre de archivo:** alcornoques_25829.shp
- **Tipo de entidad:** Shapefile de puntos
- **Qué se cartografía:** Pies de alcornoque (_Quercus suber_) dentro del Parque Nacional de Doñana.

---

## 3. Alcance espacial y temporal

- **Cobertura espacial:** Parque Nacional de Doñana  
- **Cobertura temporal:** junio-julio 2022 

> **Aviso:** no apto para deslindes ni decisiones jurídicas (si aplica).

---

## 4. Sistema de referencia (CRS)

- **CRS / EPSG:** EPSG:25829 - ETRS89 / UTM zone 29N Projected
- **Unidades:** individuos (pies) de _Quercus suber_.

---

## 5. Fuentes de datos

**Base de partida:** compilación de fuentes previas.  
**Tratamiento posterior:** la base fue ***modificada, ampliada y armonizada por el autor*** (Sección 6).

- Solís, J. C. (1996). Plan de ordenación del alcornocal de Doñana. Informe Técnico, 105 pp
- Ramo, C. & Calderón, J. (2013). Mapa y catálogo de los alcornoques centenarios de la Reserva Biológica de Doñana. 

---

## 6. Flujo de trabajo (métodos)

- **Paso 1. Compilación y depuración de bases de partida**  
  Se partió de la base de seguimiento de alcornoques de C. Ramo (incluyendo los alcornoques inventariados en Ramo & Calderón 2013). Se revisó la coherencia espacial y se **retuvieron únicamente los individuos considerados vivos hasta 2022**, excluyendo aquellos confirmados como muertos con anterioridad a 2023.  
  La base se **amplió** incorporando individuos adicionales reportados como vivos en Solís (1996), homogeneizando campos e identificadores para evitar duplicados.

- **Paso 2. Búsqueda dirigida de nuevas ocurrencias mediante fotointerpretación**  
  A partir de la base depurada, se realizó un recorrido sistemático (manual) de las principales unidades de hábitat con presencia potencial de alcornoque (manchas de **monte negro**, **vera** y **bordes de lagunas**), localizando formaciones arbóreas susceptibles de ser _Quercus suber_.

- **Paso 3. Filtrado altimétrico con modelo de superficies de vegetación**  
  Se empleó el **Modelo Digital de Superficies de Vegetación (MDSnV2,5; 2ª cobertura; ETRS89 / H29N)** para seleccionar únicamente formaciones con alturas **entre 4 y 20 m**, con el objetivo de:  
  (i) excluir masas de árboles típicamente más altos o con estructura distinta (p. ej., pinos, álamos, fresnos, eucaliptos altos) y  
  (ii) eliminar el matorral alto y otras coberturas no arbóreas.

- **Paso 4. Validación final por ortofotografía PNOA (máxima actualidad)**  
  Sobre las manchas filtradas, se realizó **fotointerpretación individualizada** utilizando la ortofotografía PNOA de máxima actualidad para Doñana (**junio–julio 2022**), confirmando la presencia de rasgos diagnósticos compatibles con alcornoque y descartando falsos positivos.

- **Paso 5. Resolución de incertidumbres con series históricas de ortofotos**  
  En casos dudosos, se consultaron ortofotografías de años previos para diferenciar manchas jóvenes (frecuentes en pinares de repoblación/expansión reciente) de individuos o rodales de mayor persistencia temporal, coherentes con el carácter centenario de los alcornoques de Doñana.

- **Paso 6. Integración, estandarización y exportación**  
  Los individuos confirmados se integraron en una única capa de puntos. Se estandarizaron atributos y se exportó el producto final como shapefile.

**Criterios clave (definiciones):**  
- **Inclusión/exclusión:**  
  - *Inclusión:* individuos o formaciones arbóreas interpretadas como _Quercus suber_ dentro del Parque Nacional de Doñana, confirmadas por fotointerpretación (PNOA 2022) y/o por presencia en bases de partida verificadas.  
  - *Exclusión:* individuos confirmados como muertos antes de 2023 (en la base de seguimiento), y manchas descartadas por rasgos no compatibles con alcornoque o por corresponder a otras especies/estructuras vegetales.

- **Umbrales/códigos:**  
  - *Filtro de altura (MDSnV2,5):* **4–20 m** (selección de formaciones arbóreas plausibles; exclusión de matorral alto y arbolado típicamente más alto).  
  - *Regla de decisión en caso de duda:* consulta de ortofotos históricas; priorización de persistencia temporal y rasgos diagnósticos compatibles con _Q. suber_.

- **Supuestos:**  
  - La ortofotografía PNOA 2022 permite identificar rasgos diagnósticos a escala de interpretación adecuada para un inventario orientativo (no jurídico).  
  - El filtro 4–20 m reduce falsos positivos, pero puede introducir falsos negativos (p. ej., individuos más bajos por estrés, regenerado o condiciones locales).  
  - La diferenciación por series históricas mejora la separación entre pinares jóvenes y formaciones de mayor antigüedad, aunque no constituye datación directa.

---

## 7. Estructura de datos y atributos

El archivo incluye un “diccionario” de campos.

| Campo | Tipo | Descripción | Unidades / códigos |
|---|---|---|---|
| ID | string | Identificador único de cada árbol | Nº consecutivo |
| Alcornoque | integer | Código individual de las tablillas marcadas | Código |
| diametro | integer | Diámetro de árbol a la altura del pecho (DAP) | Centímetros |
| coordx | integer | Coordenada X | EPSG:25829 |
| coordy | integer | Coordenada Y | EPSG:25829 |

**Valores ausentes / nulos:** _NULL_ 

<img src="{{ "/assets/img/308.jpg" | relative_url }}" alt="Topo Doñana" style="max-width: 100%; height: auto; margin: 0 0 1rem 0;">
---

## 8. Control de calidad y validación

- **Controles realizados:**  
  - **Eliminación de duplicados:** consolidación de registros procedentes de Solís (1996) y Ramo & Calderón (2013), revisando coincidencias espaciales.  
  - **Consistencia espacial:** verificación de que todos los puntos se encuentran **dentro del Parque Nacional de Doñana** y en el **CRS declarado (EPSG:25829)**.  
  - **Revisión visual sistemática:** inspección manual de cada candidato tras el filtrado (MDSnV) para descartar falsos positivos (pinares, eucaliptales, frondosas altas, matorral alto).  
  - **Reglas QA/QC básicas:** control de valores nulos en campos obligatorios (p. ej., `ID`), homogeneización de codificación y formato de atributos.

- **Validación:**  
  - **Fotointerpretación directa** sobre ortofotografía PNOA de máxima actualidad (junio–julio 2022), empleando rasgos diagnósticos de copa/estructura y contexto (ver Sección 6).  
  - **Comparación con fuentes previas**: contraste con la base de seguimiento de C. Ramo (incluyendo Ramo & Calderón 2013) y con la cartografía de Solís (1996).  
  - **Validación temporal auxiliar**: consulta de ortofotos históricas para resolver casos dudosos y discriminar pinares jóvenes frente a formaciones persistentes compatibles con alcornoques.

- **Problemas conocidos (limitaciones):**  
  - **Falsos negativos:** el filtro de altura (4–20 m) puede excluir individuos más bajos (por estrés hídrico, podas, estructuras abiertas) o alcornoques aislados parcialmente ocultos por matorral.  
  - **Falsos positivos residuales:** pese a la revisión, algunas formaciones pueden confundirse con otras frondosas o masas mixtas en áreas de sombra, mosaico denso o resolución limitada.  
  - **Sesgo de detectabilidad:** la probabilidad de detección es mayor en unidades abiertas (vera, bordes de lagunas) que en masas densas o zonas con cobertura continua.  
  - **Incertidumbre temporal:** el producto representa individuos **vivos hasta 2022** según las fuentes y la interpretación; no refleja mortalidad posterior ni reclutamiento reciente.

- **Precisión posicional (si se conoce):**    
En caso de uso analítico sensible a la posición exacta (p. ej., distancias finas), se recomienda **verificación de campo** o cotejo con fuentes GPS.

---

## 9. Limitaciones y uso apropiado

- **Usos recomendados:**  
  - Cartografía de síntesis y **visualización** de la distribución de alcornoques (_Quercus suber_) a escala de Parque Nacional.  
  - Soporte para **análisis exploratorios** (p. ej., patrones espaciales amplios, relación con unidades ambientales o proximidad a lagunas), siempre a escala compatible con la resolución efectiva del producto.  
  - **Planificación orientativa** de muestreos y prospecciones de campo (priorización de zonas, diseño de transectos, etc.).  
  - Contextualización y divulgación (información ilustrativa y comparativa entre áreas).

- **No recomendado para:**  
  - Delimitaciones legales, catastrales o decisiones administrativas/jurídicas.  
  - Uso operativo que requiera **posición exacta del tronco** (p. ej., inventarios forestales de precisión, tala/poda, actuaciones árbol a árbol) sin verificación de campo.  
  - Estimar con precisión **abundancia real** o **mortalidad** sin actualización/verdad-terreno.

**Limitaciones específicas:**  
La fotointerpretación presenta limitaciones sólo subsanables mediante la verdad-terreno; manchas densas de madroños (_Arbutus unedo_) y piruétano (_Pyrus bourgaeana_) maduros pueden confundirse con alcornoques en ortofotografía. Asimismo, aunque el mayor evento de mortalidad ocurrió durante 2023, numerosos ejemplares se encontraban ya debilitados en 2022 y es posible que no hayan sido correctamente identificados o que su estado vital haya cambiado poco después. En consecuencia, esta capa debe considerarse **orientativa** y su uso para trabajos de detalle requiere **confirmación en campo**.

---

## 10. Cita recomendada

M. de Felipe (2026). Mapa actualizado del Parque Nacional de Doñana. Zenodo. [DOI: https://doi.org/10.5281/zenodo.18109683](https://doi.org/10.5281/zenodo.18109683)

---

## 11. Historial de cambios de la capa

- **v1.0.0 (10-01-2026)** — Creación del archivo
  <!--
   **vX.Y.Z (YYYY-MM-DD)** — … -->

---

## 12. Contacto

Para dudas, sugerencias, incidencias o acceso a capas no públicas, contáctame [aqui](mailto:m.defelipe.t@gmail.com).
