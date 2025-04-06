---
layout: archive
title: "Travelling Map"
permalink: /map/
author_profile: true
---

{% include base_path %}
The places that I've visited
<html>
<head>
  <title>My Travel Map</title>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css" />
  <style>
    #map { height: 100vh; }
  </style>
</head>
<body>
  <div id="map"></div>

  <script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>
  <script>
    const map = L.map('map').setView([10, 10], 3);

    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
      attribution: '&copy; OpenStreetMap contributors'
    }).addTo(map);

    const locations = [
  [51.5074, -0.1278, "London, UK"],
  [51.4545, -2.5879, "Bristol, UK"],
  [55.8642, -4.2518, "Glasgow, UK"],
  [38.9072, -77.0369, "Washington, D.C., USA"],
  [40.7128, -74.0060, "New York, USA"],
  [49.2827, -123.1207, "Vancouver, Canada"],
  [31.2304, 121.4737, "Shanghai, China"]
];

    const pinIcon = L.icon({
      iconUrl: 'https://cdn-icons-png.flaticon.com/512/684/684908.png',
      iconSize: [32, 32],
      iconAnchor: [16, 32],
      popupAnchor: [0, -32]
    });

    locations.forEach(([lat, lng, label]) => {
      L.marker([lat, lng], { icon: pinIcon }).addTo(map).bindPopup(label);
    });
  </script>
</body>
</html>


