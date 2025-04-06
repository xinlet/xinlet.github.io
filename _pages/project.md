---
layout: archive
title: "Travelling Map"
permalink: /map/
author_profile: true
---

{% include base_path %}

<!DOCTYPE html>
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
      [5.6037, -0.1870, "Accra, Ghana"],
      [6.5244, 3.3792, "Lagos, Nigeria"],
      [9.0579, 7.4951, "Abuja, Nigeria"],
      [13.5128, 2.1120, "Niamey, Niger"],
      [12.6392, -8.0029, "Bamako, Mali"],
      [14.6928, -17.4467, "Dakar, Senegal"],
      [8.4657, -13.2317, "Freetown, Sierra Leone"],
      [6.3156, -10.8074, "Monrovia, Liberia"],
      [30.0444, 31.2357, "Cairo, Egypt"],
      [33.3128, 44.3615, "Baghdad, Iraq"],
      [25.276987, 55.296249, "Dubai, UAE"],
      [19.0760, 72.8777, "Mumbai, India"],
      [28.6139, 77.2090, "New Delhi, India"]
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


