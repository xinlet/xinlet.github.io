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
  [53.38038466992851, -1.4692677986880176, "Sheffield, UK"],
  [53.96161935398514, -1.0744123379947363, "York, UK"],
  [53.479981699809294, -2.2378846016945113, "Manchester, UK"],
  [51.454979536371034, -0.979225516110098, "Reading, UK"],
  [41.15727108920829, -8.626760871139524, "Porto, Portugal"],
  [41.545468852024115, -8.426184776233601, "Braga, Portugal"],
  [52.52260846062111, 13.396570401973973, "Berlin, Germany"],
  [50.07541988802119, 14.45737474520111, "Prague, Czechia"],
  [48.85814790470617, 2.3532114719243884, "Paris, France"],
  [38.907302990574024, -77.03924041214798, "Washington, D.C., USA"],
  [39.28943603208796, -76.60345755408721, "Baltimore, USA"],
  [40.712430367670926, -74.00536100889536, "New York, USA"],
  [41.878087294002086, -87.63369974212341, "Chicago, USA"],
  [38.882996720153166, -77.082147911314, "Arlington, USA"],
  [38.989228065641605, -76.93454772018893, "College Park, USA"],
  [42.355570680454484, -71.0580566051323, "Boston, USA"],
  [37.77328546687444, -122.42200607366087, "San Francisco, USA"],
  [49.26026987939737, -123.24548460509973, "Vancouver, Canada"],
  [49.28581226882002, -122.78103632909878, "Coquitlam, Canada"],
  [49.25049704518672, -122.97597724313502, "Burnaby, Canada"],
  [49.16083705619697, -123.94126246836784, "Nanaimo, Canada"],
  [49.166286372260274, -123.13325633925318, "Richmond, Canada"],
  [48.428257631971555, -123.36420083510893, "Victoria, Canada"],
  [31.239194119807333, 121.47258153801539, "Shanghai, China"],
  [31.3037517759364, 120.59092874064407, "Suzhou, China"],
  [32.050107326542594, 118.85922013237372, "Nanjing, China"],
  [32.398217452736866, 119.40974939622839, "Yangzhou, China"],
  [22.324060634176035, 114.17371834319583, "Hongkong, China"],
  [22.547833044249305, 114.04735874974526, "Shenzhen, China"],
  [39.90998150383738, 116.40428002417717, "Beijing, China"],
  [30.581607263940185, 104.06248714859332, "Chengdu, China"],
  [23.129044018551806, 113.25113428264531, "Guangzhou, China"]，
  [41.80823225730331, 123.43535864197163, "Shenyang, China"],
  [37.55473948615032, 126.98918615170025, "Seoul, Korea"]
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


