---
layout: default
title: "Lagunas"
permalink: /es/content/lagunas/
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

# Cartografía de la red de lagunas del Parque Nacional de Doñana - Ficha de capa

> **Fuente oficial (metadatos + descarga):** [Registro REDIAM](https://portalrediam.cica.es/geonetwork/srv/api/records/db48f197-a17f-4f86-9e66-447da049f18c)  
> **Descarga (en este repositorio):** *[Zenodo](https://doi.org/10.5281/zenodo.18109683)*.
>
> **Versión:** v1.0.0 · **Última actualización:** 10-01-2026  
>**Licencia:** CC BY-NC 4.0

> **Condiciones de uso:** consultar las restricciones/condiciones indicadas en la ficha oficial de REDIAM.

---

## 1. Resumen

Esta capa contiene la delimitación vectorial de las **lagunas temporales** del Parque Nacional de Doñana, distribuida por la Junta de Andalucía a través de **REDIAM**. El producto original incluye su propia ficha de metadatos y documentación asociada.

**Autoría del dato:** esta capa no ha sido producida por el autor de esta web, sino por *C. Gómez-Rodríguez, C. Díaz-Paniagua & J. Bustamante (2011)*.

**Motivo de inclusión en este repositorio:** se incluye una copia para facilitar su descarga centralizada dentro del proyecto, remitiendo siempre a la ficha oficial de REDIAM como referencia primaria de metadatos, alcance y condiciones.

---

## 2. Contenido

- **Nombre de capa (REDIAM):** Cartografía de las lagunas temporales del Parque Nacional de Doñana  
- **Tipo de entidad:** Polígonos  
- **Qué se cartografía:** lagunas temporales del Parque Nacional de Doñana.  

---

## 3. Alcance espacial y temporal

- **Cobertura espacial:** Parque Nacional de Doñana.  
- **Cobertura temporal (referencia del producto):** Máxima inundación en primavera de 2004; consultar la documentación asociada en REDIAM (metodología y fechas de referencia).  
- **Escala/uso recomendado:** consultar la ficha oficial de REDIAM.

---

## 4. Sistema de referencia (CRS)

- **CRS / EPSG (según REDIAM):** EPSG 25829 / ETRS89 UTM zona 29N (EPSG:23030 en REDIAM)  
- **Unidades:** metros.  

---

## 5. Fuentes de datos

**Fuente primaria (oficial):**  
- *Gómez-Rodríguez, C., Díaz-Paniagua, C. & Bustamante, J. (2011). Cartografía de las lagunas temporales del Parque Nacional de Doñana. Agencia Andaluza del Agua. Consejería de Medio Ambiente. Junta de Andalucía.*


**Documentación asociada (disponible en REDIAM):**  
- *Modelo de Datos Geográficos* (estructura de campos y tipos).  
- Memoria/Informe(s) del producto (metodología, alcance, limitaciones).

**Nota sobre redistribución:** esta web/repositorio ofrece una copia “de conveniencia” para su descarga dentro del proyecto; la referencia oficial de metadatos y restricciones debe tomarse del registro REDIAM.

---

## 6. Flujo de trabajo (métodos)

*No aplica*

---

## 7. Estructura de datos y atributos (según REDIAM)

### Campos del producto empleado en el proyecto

**Nombre:** 'pondcartography_25829.shp'

| Campo | Tipo | Descripción |
|---|---|---|
| `fid` | (OID) | Identificador interno |
| `COORDX` | (Double) | Coordenada X (EPSG:25829) |
| `COORDY` | (Double) | Coordenada Y (EPSG:25829) |
| `AREA` | (Double) | Área de máxima inundación de la laguna |
| `ID_LAGTEMP` | (Double) | Identificador/código de laguna |
| `TOPONIMO` | (String) | Nombre/topónimo de la laguna |

---

## 8. Control de calidad y validación

 Consultar la documentación asociada en REDIAM (metodología y evaluación de errores).

---

## 9. Limitaciones y uso apropiado

- **Usos recomendados:**  
  - Visualización y análisis exploratorio a escala de parque.  
  - Apoyo a prospecciones y planificación de muestreo, manteniendo la escala recomendada por el producto.

- **No recomendado para:**  
  - Delimitaciones legales/jurídicas o decisiones que requieran precisión de detalle sin verificación específica.  
  - Interpretaciones fuera del alcance temporal/metodológico descrito en el producto original.

---

## 10. Citación

**Cita recomendada:**  
Gómez-Rodríguez, C., Díaz-Paniagua, C. & Bustamante, J. (2011). Cartografía de las lagunas temporales del Parque Nacional de Doñana. Agencia Andaluza del Agua. Consejería de Medio Ambiente.Junta de Andalucía. 

Registro: [https://portalrediam.cica.es/geonetwork/srv/api/records/db48f197-a17f-4f86-9e66-447da049f18c](https://portalrediam.cica.es/geonetwork/srv/api/records/db48f197-a17f-4f86-9e66-447da049f18c)

---

## 11. Historial de cambios (en este repositorio)

- **v1.0.0 (10-01-2026)** — Inclusión de copia del producto REDIAM y versión con atributos mínimos (sin modificación geométrica).

---

## 12. Contacto

Para dudas sobre el repositorio del proyecto: contáctame [aqui](mailto:m.defelipe.t@gmail.com)  
Para cuestiones oficiales de metadatos/distribución del dataset: ver contacto en la ficha de REDIAM.
