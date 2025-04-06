---
layout: archive
title: "The places that I've visited/lived"
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
    const map = L.map('map', {
  worldCopyJump: false,
  minZoom: 2
}).setView([54, -2], 4);

    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
  attribution: '&copy; OpenStreetMap contributors',
  noWrap: true
}).addTo(map);

    const locations = [
  [51.50609700613507, -0.13100357699231469, "London, UK"],
  [51.454221808102815, -2.5878198663371585, "Bristol, UK"],
  [51.37793543104405, -2.359340173854564, "Bath, UK"],
  [52.4795103752684, -1.8879851605385491, "Birmingham, UK"],
  [52.955028180927144, -1.1553010969961675, "Nottingham, UK"],   
  [55.867493903697664, -4.252465435368384, "Glasgow, UK"],
  [51.75149898185093, -1.2542533195511452, "Oxford, UK"],
  [52.62901549787241, 1.2995397492799585, "Norwich, UK"],
  [52.188114934404865, 0.2006293284257205, "Cambridge, UK"],
  [54.04407139344605, -2.8011226811415875, "Lancaster, UK"],
  [53.3691450738658, -1.370797786126028, "Sheffield, UK"],
  [53.96011481834575, -1.0220066724283572, "York, UK"],
  [53.480675548580244, -1.9411023500726563, "Manchester, UK"],
  [41.15727108920829, -8.626760871139524, "Porto, Portugal"],
  [41.545468852024115, -8.426184776233601, "Braga, Portugal"],
  [52.52260846062111, 13.396570401973973, "Berlin, Germany"],
  [50.07541988802119, 14.45737474520111, "Prague, Czechia"],
  [48.85814790470617, 2.3532114719243884, "Paris, France"],
  [38.905669551870176, -77.02064942344595, "Washington, D.C., USA"],
  [39.28943603208796, -76.60345755408721, "Baltimore, USA"],
  [40.70083265111221, -73.39742067505556, "New York, USA"],
  [41.81853384049103, -86.92999305273052, "Chicago, USA"],
  [38.882996720153166, -77.082147911314, "Arlington, USA"],
  [38.989228065641605, -76.93454772018893, "College Park, USA"],
  [42.325894662704755, -70.83710518059979, "Boston, USA"],
  [49.285208747911675, -123.05859945681277, "Vancouver, Canada"],
  [49.28581226882002, -122.78103632909878, "Coquitlam, Canada"],
  [49.25049704518672, -122.97597724313502, "Burnaby, Canada"],
  [49.16083705619697, -123.94126246836784, "Nanaimo, Canada"],
  [37.72916079679282, -121.33854919209256, "San Francisco, USA"],
  [31.16605804034499, 121.97030953947004, "Shanghai, China"],
  [31.3037517759364, 120.59092874064407, "Suzhou, China"],
  [22.324060634176035, 114.17371834319583, "Hongkong, China"],
  [22.547833044249305, 114.04735874974526, "Shenzhen, China"],
  [39.846900911268605, 117.11803173117819, "Beijing, China"],
  [30.501906428973715, 104.46055406371309, "Chengdu, China"]
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


