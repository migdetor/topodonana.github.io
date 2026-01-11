---
layout: default
title: "Mapa ineractivo"
permalink: /es/interactive/
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

<link
  rel="stylesheet"
  href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css"
/>

<style>
  #map {
    height: 80vh;
    min-height: 520px;
    width: 100%;
    margin: 0 0 1rem 0;
    border-radius: 8px;
  }
</style>

<div id="map"></div>

<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>

<script>
  // Centro aproximado de Doñana (ajusta si quieres)
  const map = L.map("map", {
    center: [37.0, -6.5],
    zoom: 11
  });

  // Base satélite (tipo Google)
  const esriSat = L.tileLayer(
    "https://server.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer/tile/{z}/{y}/{x}",
    {
      maxZoom: 19,
      attribution: "Tiles &copy; Esri"
    }
  ).addTo(map);

  // Base alternativa
  const osm = L.tileLayer(
    "https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",
    {
      maxZoom: 19,
      attribution: "&copy; OpenStreetMap contributors"
    }
  );

  // Tu mapa como overlay (AJUSTA extensión si no es .jpg)
  const topoDonana = L.tileLayer(
    "{{ '/assets/tiles/topodonana/{z}/{x}/{y}.png' | relative_url }}",
    {
      minZoom: 10,
      maxZoom: 14,
      opacity: 0.9
    }
  ).addTo(map);

  const baseLayers = {
    "Satélite": esriSat,
    "OpenStreetMap": osm
  };

  const overlays = {
    "Mi mapa (Topo Doñana)": topoDonana
  };

  L.control.layers(baseLayers, overlays, { collapsed: false }).addTo(map);
</script>
