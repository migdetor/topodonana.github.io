---
layout: default
title: Mapa ineractivo
permalink: /es/interactive/
---

---
layout: default
title: Mapa interactivo
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
  // Centro aproximado de Doñana
  const map = L.map("map", {
    center: [37.0, -6.5],
    zoom: 10,
    minZoom: 10,
    maxZoom: 11
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

  // Tu mapa como overlay (tiles PNG)
  // Ajusta "topodonana" si tu carpeta tiene otro nombre
  const topoDonana = L.tileLayer(
    "{{ '/assets/tiles/topodonana/{z}/{x}/{y}.png' | relative_url }}",
    {
      minZoom: 10,
      maxZoom: 11,
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
