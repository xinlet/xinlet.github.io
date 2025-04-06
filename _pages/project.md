---
layout: archive
title: "The places that I've visited"
permalink: /map/
author_profile: true
---

{% include base_path %}

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
  [51.3780, -2.3580, "Bath, UK"],
  [52.4795103752684, -1.8879851605385491, "Birmingham, UK"],
  [52.955028180927144, -1.1553010969961675, "Nottingham, UK"],   
  [55.8642, -4.2518, "Glasgow, UK"],
  [51.7507, -1.2580, "Oxford, UK"],
  [52.1949, 0.1330, "Cambridge, UK"],
  [41.15727108920829, -8.626760871139524, "Porto, Portugal"],
  [41.545468852024115, -8.426184776233601, "Braga, Portugal"],
  [52.52260846062111, 13.396570401973973, "Berlin, Germany"],
  [50.07541988802119, 14.45737474520111, "Prague, Czechia"],
  [48.85814790470617, 2.3532114719243884, "Paris, France"],
  [38.9072, -77.0369, "Washington, D.C., USA"],
  [40.7128, -74.0060, "New York, USA"],
  [41.8760, -87.6336, "Chicago, USA"],
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


